<template>
  <div class="min-h-screen">

    <!-- Navigation -->
    <nav class="fixed top-0 left-0 right-0 z-50 transition-all duration-300"
         :class="scrolled ? 'bg-white/80 backdrop-blur-lg shadow-sm border-b border-gray-100' : 'bg-transparent'">
      <div class="max-w-6xl mx-auto px-6 py-4 flex items-center justify-between">
        <a href="#" class="text-lg font-bold text-brand-700">سادگی کد</a>
        <div class="hidden md:flex items-center gap-8 text-sm font-medium text-gray-600">
          <a href="#learn" class="hover:text-brand-600 transition">آنچه یاد می‌گیرید</a>
          <a href="#chapters" class="hover:text-brand-600 transition">فهرست فصل‌ها</a>
          <a href="#reviews" class="hover:text-brand-600 transition">نظرات</a>
          <a href="#faq" class="hover:text-brand-600 transition">سوالات متداول</a>
        </div>
        <a href="#buy" class="bg-brand-600 text-white px-5 py-2 rounded-lg text-sm font-semibold hover:bg-brand-700 transition shadow-md shadow-brand-600/20">
          خرید کتاب
        </a>
      </div>
    </nav>

    <!-- Hero Section -->
    <header class="relative pt-32 pb-20 lg:pt-40 lg:pb-32 overflow-hidden">
      <!-- Background -->
      <div class="absolute inset-0 bg-gradient-to-bl from-brand-50 via-white to-indigo-50"></div>
      <div class="absolute top-0 left-0 w-full h-full opacity-[0.03]" style="background-image: url('data:image/svg+xml,<svg width=&quot;60&quot; height=&quot;60&quot; viewBox=&quot;0 0 60 60&quot; xmlns=&quot;http://www.w3.org/2000/svg&quot;><g fill=&quot;none&quot; fill-rule=&quot;evenodd&quot;><g fill=&quot;%234263eb&quot; fill-opacity=&quot;1&quot;><path d=&quot;M36 34v-4h-2v4h-4v2h4v4h2v-4h4v-2h-4zm0-30V0h-2v4h-4v2h4v4h2V6h4V4h-4zM6 34v-4H4v4H0v2h4v4h2v-4h4v-2H6zM6 4V0H4v4H0v2h4v4h2V6h4V4H6z&quot;/></g></g></svg>');"></div>
      <div class="absolute -top-32 -left-32 w-96 h-96 bg-brand-200/30 rounded-full blur-3xl"></div>
      <div class="absolute -bottom-20 -right-20 w-80 h-80 bg-indigo-200/20 rounded-full blur-3xl"></div>

      <div class="relative max-w-6xl mx-auto px-6 flex flex-col-reverse lg:flex-row items-center gap-12 lg:gap-20">
        <!-- Text -->
        <div class="flex-1 text-center lg:text-right">
          <div class="inline-block bg-brand-100 text-brand-700 text-xs font-semibold px-3 py-1 rounded-full mb-6">
            ترجمه فارسی کتاب Code Simplicity
          </div>
          <h1 class="text-4xl sm:text-5xl lg:text-6xl font-black text-gray-900 leading-tight mb-6">
            سادگی کد
          </h1>
          <p class="text-lg sm:text-xl text-gray-600 leading-relaxed mb-4 max-w-lg mx-auto lg:mx-0 lg:ml-0">
            علم و هنر نوشتن کدهایی که <strong class="text-gray-800">ساده، پایدار و قابل نگهداری</strong> هستند.
          </p>
          <p class="text-sm text-gray-500 mb-8">
            نوشته <strong>مکس کانات-الکساندر</strong> &bull; ترجمه <strong>مسلم دریس جرفی</strong>
          </p>

          <!-- Purchase Buttons -->
          <div id="buy" class="flex flex-wrap justify-center lg:justify-start gap-3">
            <a v-for="(link, idx) in purchaseLinks" :key="idx" :href="link.url" target="_blank" rel="noopener"
               class="group flex items-center gap-2 bg-white border border-gray-200 text-gray-700 px-5 py-2.5 rounded-xl text-sm font-medium shadow-sm hover:shadow-md hover:border-brand-300 hover:text-brand-700 transition-all duration-200">
              <span v-html="link.icon"></span>
              {{ link.label }}
              <svg class="w-3.5 h-3.5 opacity-0 -translate-x-1 group-hover:opacity-100 group-hover:translate-x-0 transition-all" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7"/></svg>
            </a>
          </div>
        </div>

        <!-- Book Cover -->
        <div class="relative flex-shrink-0">
          <div class="absolute -inset-4 bg-gradient-to-br from-brand-400/20 to-indigo-400/20 rounded-3xl blur-2xl"></div>
          <div class="relative bg-white p-3 rounded-2xl shadow-2xl shadow-brand-900/10 ring-1 ring-gray-100">
            <img
              src="https://www.motekhassesan.com/wp-content/uploads/2025/03/r-25.jpg"
              alt="جلد کتاب سادگی کد - ترجمه فارسی Code Simplicity اثر مکس کانات-الکساندر"
              class="w-56 sm:w-64 lg:w-72 rounded-xl"
              width="288"
              height="400"
              loading="eager"
            />
          </div>
        </div>
      </div>
    </header>

    <main>
      <!-- What You'll Learn -->
      <section id="learn" class="py-20 lg:py-28">
        <div class="max-w-6xl mx-auto px-6">
          <div class="text-center mb-14">
            <h2 class="text-3xl sm:text-4xl font-extrabold text-gray-900 mb-4">با خواندن این کتاب چه یاد می‌گیرید؟</h2>
            <p class="text-gray-500 text-lg max-w-2xl mx-auto">اصول بنیادینی که هر توسعه‌دهنده‌ای برای نوشتن کد بهتر به آن‌ها نیاز دارد</p>
          </div>
          <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
            <div v-for="(item, idx) in learnings" :key="idx"
                 class="group bg-white rounded-2xl p-7 border border-gray-100 shadow-sm hover:shadow-lg hover:border-brand-200 transition-all duration-300">
              <div class="w-12 h-12 rounded-xl flex items-center justify-center text-2xl mb-5"
                   :class="item.bgColor">
                {{ item.icon }}
              </div>
              <h3 class="text-lg font-bold text-gray-900 mb-2">{{ item.title }}</h3>
              <p class="text-gray-500 text-sm leading-relaxed">{{ item.desc }}</p>
            </div>
          </div>
        </div>
      </section>

      <!-- Chapters -->
      <section id="chapters" class="py-20 lg:py-28 bg-gradient-to-b from-gray-50 to-white">
        <div class="max-w-4xl mx-auto px-6">
          <div class="text-center mb-14">
            <h2 class="text-3xl sm:text-4xl font-extrabold text-gray-900 mb-4">فهرست فصل‌های کتاب</h2>
            <p class="text-gray-500 text-lg">شش فصل کلیدی که مسیر سادگی در کدنویسی را نشان می‌دهند</p>
          </div>
          <div class="space-y-4">
            <div v-for="(chapter, idx) in chapters" :key="idx"
                 class="flex items-start gap-5 bg-white rounded-xl p-5 border border-gray-100 shadow-sm hover:shadow-md transition-all duration-200">
              <div class="flex-shrink-0 w-10 h-10 rounded-lg bg-brand-50 text-brand-600 font-bold text-lg flex items-center justify-center">
                {{ idx + 1 }}
              </div>
              <div>
                <h3 class="font-bold text-gray-900">{{ chapter.title }}</h3>
                <p class="text-sm text-gray-500 mt-1">{{ chapter.desc }}</p>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- Testimonials -->
      <section id="reviews" class="py-20 lg:py-28">
        <div class="max-w-6xl mx-auto px-6">
          <div class="text-center mb-14">
            <h2 class="text-3xl sm:text-4xl font-extrabold text-gray-900 mb-4">نظرات خوانندگان</h2>
            <p class="text-gray-500 text-lg">برنامه‌نویسانی که از خواندن این کتاب بهره برده‌اند</p>
          </div>
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
            <article v-for="(review, idx) in reviews" :key="idx"
                     class="relative bg-white rounded-2xl p-8 border border-gray-100 shadow-sm">
              <svg class="absolute top-6 left-6 w-8 h-8 text-brand-100" fill="currentColor" viewBox="0 0 24 24"><path d="M14.017 21v-7.391c0-5.704 3.731-9.57 8.983-10.609l.995 2.151c-2.432.917-3.995 3.638-3.995 5.849h4v10h-9.983zm-14.017 0v-7.391c0-5.704 3.748-9.57 9-10.609l.996 2.151c-2.433.917-3.996 3.638-3.996 5.849h3.983v10h-9.983z"/></svg>
              <blockquote class="text-gray-700 leading-relaxed mb-6 pr-0 pt-2">
                {{ review.text }}
              </blockquote>
              <footer class="flex items-center gap-3 border-t border-gray-100 pt-4">
                <div class="w-10 h-10 rounded-full flex items-center justify-center text-white font-bold text-sm"
                     :class="review.avatarColor">
                  {{ review.name.charAt(0) }}
                </div>
                <div>
                  <cite class="not-italic font-semibold text-gray-900 text-sm">{{ review.name }}</cite>
                  <p class="text-xs text-gray-400">{{ review.role }}</p>
                </div>
              </footer>
            </article>
          </div>
        </div>
      </section>

      <!-- FAQ -->
      <section id="faq" class="py-20 lg:py-28 bg-gradient-to-b from-gray-50 to-white">
        <div class="max-w-3xl mx-auto px-6">
          <div class="text-center mb-14">
            <h2 class="text-3xl sm:text-4xl font-extrabold text-gray-900 mb-4">سوالات متداول</h2>
            <p class="text-gray-500 text-lg">پاسخ به رایج‌ترین سوالات درباره کتاب سادگی کد</p>
          </div>
          <div class="space-y-4">
            <details v-for="(faq, idx) in faqs" :key="idx"
                     class="group bg-white rounded-xl border border-gray-100 shadow-sm overflow-hidden">
              <summary class="flex items-center justify-between cursor-pointer p-6 font-semibold text-gray-900 hover:text-brand-700 transition select-none">
                {{ faq.q }}
                <svg class="w-5 h-5 text-gray-400 group-open:rotate-180 transition-transform flex-shrink-0" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"/></svg>
              </summary>
              <div class="px-6 pb-6 text-gray-600 leading-relaxed border-t border-gray-50 pt-4">
                {{ faq.a }}
              </div>
            </details>
          </div>
        </div>
      </section>

      <!-- About Translator -->
      <section class="py-20 lg:py-28">
        <div class="max-w-4xl mx-auto px-6">
          <div class="bg-gradient-to-bl from-brand-600 to-brand-800 rounded-3xl p-10 sm:p-14 text-center text-white relative overflow-hidden">
            <div class="absolute top-0 left-0 w-full h-full opacity-10" style="background-image: url('data:image/svg+xml,<svg width=&quot;40&quot; height=&quot;40&quot; viewBox=&quot;0 0 40 40&quot; xmlns=&quot;http://www.w3.org/2000/svg&quot;><circle cx=&quot;20&quot; cy=&quot;20&quot; r=&quot;1.5&quot; fill=&quot;white&quot;/></svg>');"></div>
            <div class="relative">
              <h2 class="text-3xl sm:text-4xl font-extrabold mb-4">درباره مترجم</h2>
              <p class="text-2xl font-bold text-brand-100 mb-4">مسلم دریس جرفی</p>
              <p class="text-brand-200 text-lg leading-relaxed max-w-xl mx-auto mb-8">
                برنامه‌نویس و مترجم علاقه‌مند به سادگی در طراحی نرم‌افزار.
                با هدف انتقال دانش برنامه‌نویسی به زبان فارسی، این کتاب را ترجمه کرده است.
              </p>
              <a href="#buy" class="inline-flex items-center gap-2 bg-white text-brand-700 px-8 py-3 rounded-xl font-bold text-sm hover:bg-brand-50 transition shadow-lg">
                همین حالا کتاب را تهیه کنید
                <svg class="w-4 h-4 rotate-180" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"/></svg>
              </a>
            </div>
          </div>
        </div>
      </section>
    </main>

    <!-- Footer -->
    <footer class="border-t border-gray-100 bg-white">
      <div class="max-w-6xl mx-auto px-6 py-8 flex flex-col sm:flex-row items-center justify-between gap-4 text-sm text-gray-400">
        <p>&copy; {{ currentYear }} مسلم دریس جرفی. تمامی حقوق محفوظ است.</p>
        <div class="flex items-center gap-6">
          <a v-for="(link, idx) in purchaseLinks" :key="idx" :href="link.url" target="_blank" rel="noopener"
             class="hover:text-brand-600 transition">
            {{ link.label }}
          </a>
        </div>
      </div>
    </footer>

  </div>
</template>

<script>
export default {
  name: 'LandingPage',
  data() {
    return {
      scrolled: false,
      currentYear: new Date().getFullYear(),
      purchaseLinks: [
        { label: 'دیجی‌کالا', url: 'https://www.digikala.com/product/dkp-18606281/', icon: '&#x1F6D2;' },
        { label: 'سایت انتشارات', url: 'https://www.motekhassesan.com/?p=52527', icon: '&#x1F3E2;' },
        { label: 'طاقچه', url: 'https://taaghche.com/book/226467/سادگی-کد', icon: '&#x1F4F1;' },
        { label: 'فراکتاب', url: 'https://www.faraketab.ir/book/514866-سادگی-کد', icon: '&#x1F4DA;' },
      ],
      learnings: [
        { icon: '&#x1F4D0;', title: 'اصول سادگی در کدنویسی', desc: 'یاد بگیرید چرا سادگی مهم‌ترین ویژگی یک کد خوب است و چگونه آن را به دست آورید.', bgColor: 'bg-blue-50' },
        { icon: '&#x1F4B0;', title: 'کاهش هزینه‌های نگهداری', desc: 'درک کنید چگونه طراحی ساده می‌تواند هزینه‌های نگهداری نرم‌افزار را به شدت کاهش دهد.', bgColor: 'bg-green-50' },
        { icon: '&#x1F504;', title: 'قانون تغییر', desc: 'با قانون تغییر آشنا شوید و بدانید چگونه کدی بنویسید که در برابر تغییرات مقاوم باشد.', bgColor: 'bg-amber-50' },
        { icon: '&#x1F9E0;', title: 'تصمیم‌گیری بهتر در طراحی', desc: 'ابزارها و اصولی برای تصمیم‌گیری بهتر در طراحی سیستم‌های نرم‌افزاری کسب کنید.', bgColor: 'bg-purple-50' },
        { icon: '&#x1F680;', title: 'افزایش بهره‌وری تیم', desc: 'بدانید چگونه سادگی کد به بهره‌وری بالاتر تیم توسعه و سرعت بیشتر منجر می‌شود.', bgColor: 'bg-rose-50' },
        { icon: '&#x1F3AF;', title: 'کد آینده‌دار بنویسید', desc: 'تکنیک‌هایی برای نوشتن کدی که نه‌تنها امروز، بلکه در آینده نیز قابل استفاده باشد.', bgColor: 'bg-teal-50' },
      ],
      chapters: [
        { title: 'چرا سادگی مهم است؟', desc: 'مقدمه‌ای بر اهمیت سادگی در توسعه نرم‌افزار و تاثیر آن بر موفقیت پروژه‌ها.' },
        { title: 'قانون تغییر', desc: 'چگونه تغییرات اجتناب‌ناپذیر هستند و چرا کد ما باید برای تغییر آماده باشد.' },
        { title: 'پیچیدگی و هزینه', desc: 'رابطه مستقیم بین پیچیدگی کد و هزینه‌های توسعه و نگهداری نرم‌افزار.' },
        { title: 'طراحی ساده در عمل', desc: 'روش‌ها و تکنیک‌های عملی برای پیاده‌سازی طراحی ساده در پروژه‌های واقعی.' },
        { title: 'کد آینده‌دار', desc: 'اصول و قواعدی برای نوشتن کدی که در گذر زمان ارزش خود را حفظ می‌کند.' },
        { title: 'چک‌لیست سادگی', desc: 'فهرستی کاربردی از نکاتی که به شما کمک می‌کند سادگی را در کدنویسی رعایت کنید.' },
      ],
      reviews: [
        {
          text: 'این کتاب مفاهیم عمیق و مهم را با زبانی فوق‌العاده ساده و روان منتقل می‌کند. بعد از خواندن این کتاب، نگاه من به طراحی نرم‌افزار کاملا تغییر کرد. خواندنش را به هر برنامه‌نویسی توصیه می‌کنم!',
          name: 'علی رضایی',
          role: 'توسعه‌دهنده ارشد',
          avatarColor: 'bg-brand-600',
        },
        {
          text: 'سادگی در توسعه نرم‌افزار را بهتر از هر منبع دیگری درک کردم. این کتاب یک راهنمای واقعی برای هر کسی است که می‌خواهد کد تمیزتر و حرفه‌ای‌تری بنویسد.',
          name: 'سارا محمودی',
          role: 'معمار نرم‌افزار',
          avatarColor: 'bg-indigo-500',
        },
      ],
      faqs: [
        {
          q: 'این کتاب برای چه کسانی مناسب است؟',
          a: 'این کتاب برای تمام سطوح برنامه‌نویسان، از مبتدی تا حرفه‌ای، و همچنین معماران نرم‌افزار مناسب است. هر کسی که می‌خواهد کد تمیزتر و قابل نگهداری‌تری بنویسد از مطالعه این کتاب بهره‌مند خواهد شد.',
        },
        {
          q: 'آیا مطالعه‌ کتاب نیاز به تجربه زیادی دارد؟',
          a: 'خیر. مفاهیم کتاب با زبانی ساده و قابل فهم بیان شده‌اند و نیازی به تجربه زیاد ندارد. حتی برنامه‌نویسان تازه‌کار هم می‌توانند از این کتاب استفاده کنند.',
        },
        {
          q: 'آیا نسخه دیجیتال (الکترونیکی) کتاب موجود است؟',
          a: 'بله، نسخه دیجیتال کتاب در فروشگاه‌های طاقچه و فراکتاب موجود است و می‌توانید آن را به صورت آنلاین خریداری و مطالعه کنید.',
        },
        {
          q: 'آیا این کتاب فقط برای زبان برنامه‌نویسی خاصی کاربرد دارد؟',
          a: 'خیر. اصول مطرح‌شده در این کتاب فراتر از هر زبان برنامه‌نویسی خاصی هستند و برای همه توسعه‌دهندگان، صرف‌نظر از زبان یا فریم‌ورک مورد استفاده، کاربردی هستند.',
        },
      ],
    }
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll)
  },
  beforeUnmount() {
    window.removeEventListener('scroll', this.handleScroll)
  },
  methods: {
    handleScroll() {
      this.scrolled = window.scrollY > 20
    },
  },
}
</script>

<style scoped>
details summary::-webkit-details-marker {
  display: none;
}
details summary::marker {
  display: none;
  content: '';
}
</style>
