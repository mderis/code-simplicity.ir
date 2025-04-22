<template>
  <div dir="rtl" class="relative bg-white font-sans text-gray-800 tracking-tight overflow-hidden">

    <!-- Floating Background Bubbles (Top) -->
    <div class="absolute -top-40 -left-40 w-[500px] h-[500px] bg-purple-300 rounded-full mix-blend-multiply filter blur-3xl opacity-30 animate-pulse"></div>
    <div class="absolute top-20 right-[-120px] w-[400px] h-[400px] bg-pink-300 rounded-full mix-blend-multiply filter blur-2xl opacity-40 animate-pulse delay-200"></div>
    <div class="absolute bottom-[-200px] left-10 w-[600px] h-[600px] bg-indigo-200 rounded-full mix-blend-multiply filter blur-[120px] opacity-20 animate-pulse delay-300"></div>

    <!-- Floating Background Bubbles (Lower Sections) -->
    <div class="absolute top-[1200px] right-[-180px] w-[500px] h-[500px] bg-blue-300 rounded-full mix-blend-multiply filter blur-3xl opacity-20 animate-pulse delay-300"></div>
    <div class="absolute top-[1800px] left-[-150px] w-[450px] h-[450px] bg-purple-200 rounded-full mix-blend-multiply filter blur-2xl opacity-25 animate-pulse delay-500"></div>
    <div class="absolute top-[2400px] right-[80px] w-[350px] h-[350px] bg-pink-300 rounded-full mix-blend-multiply filter blur-2xl opacity-20 animate-pulse delay-[700ms]"></div>

    <!-- Page Content -->
    <div class="relative z-10">

      <!-- Hero Section -->
      <section class="relative min-h-[80vh] flex items-center overflow-hidden">
        <div class="max-w-6xl mx-auto px-6 md:px-12 w-full flex flex-col-reverse lg:flex-row items-center gap-14 z-10">
          <div class="flex-1 text-center lg:text-right bg-white/40 backdrop-blur-md p-8 rounded-3xl shadow-xl border border-white/30">
            <h1 class="text-5xl font-extrabold text-gray-900 mb-4 leading-snug">سادگی کد</h1>
            <h2 class="text-xl text-gray-700 mb-6">ترجمه فارسی کتاب Code Simplicity</h2>
            <p class="text-sm text-gray-600 mb-4">نوشته مکس کانات-الکساندر | ترجمه: مسلم دریس جرفی</p>
            <div class="flex flex-wrap justify-center lg:justify-start gap-3 mt-6">
              <a v-for="(link, label) in purchaseLinks" :key="label" :href="link" target="_blank"
                 class="bg-white/60 text-indigo-700 backdrop-blur-sm px-4 py-2 rounded-xl shadow-md border border-indigo-200 hover:bg-white transition">
                {{ label }}
              </a>
            </div>
          </div>
          <div class="bg-white/30 border border-white/30 backdrop-blur-md p-4 rounded-3xl shadow-2xl">
            <img
                src="https://file1.cdn.faraketab.ir/content_file/content-1-514866-1088371/%D8%B3%D8%A7%D8%AF%DA%AF%DB%8C%20%DA%A9%D8%AF.avif"
                alt="جلد کتاب سادگی کد"
                class="w-64 rounded-xl"
            />
          </div>
        </div>
      </section>

      <!-- What You’ll Learn -->
      <section class="py-20 px-6">
        <div class="max-w-4xl mx-auto text-center bg-white/40 backdrop-blur-md rounded-2xl p-10 border border-white/30 shadow-md">
          <h3 class="text-2xl font-bold mb-6 text-gray-900">چه چیزهایی یاد می‌گیرید؟</h3>
          <ul class="grid grid-cols-1 sm:grid-cols-2 gap-5 text-right text-gray-700">
            <li>📘 اصول سادگی در توسعه نرم‌افزار</li>
            <li>🔧 کاهش هزینه‌های نگهداری کد</li>
            <li>📐 قانون تغییر و قانون آینده</li>
            <li>🧠 تصمیم‌گیری بهتر در طراحی سیستم</li>
            <li>🚀 افزایش بهره‌وری تیم‌های توسعه</li>
          </ul>
        </div>
      </section>

      <!-- What's Inside -->
      <section class="py-20 px-6">
        <div class="max-w-4xl mx-auto text-center bg-white/40 backdrop-blur-md rounded-2xl p-10 border border-white/30 shadow-md">
          <h3 class="text-2xl font-bold mb-6 text-gray-900">فهرست مطالب کتاب</h3>
          <ul class="list-disc pr-5 space-y-2 text-right text-gray-700">
            <li>فصل ۱: چرا سادگی مهم است؟</li>
            <li>فصل ۲: قانون تغییر</li>
            <li>فصل ۳: پیچیدگی و هزینه</li>
            <li>فصل ۴: طراحی ساده در عمل</li>
            <li>فصل ۵: کد آینده‌دار</li>
            <li>فصل ۶: چک‌لیست سادگی</li>
          </ul>
        </div>
      </section>

      <!-- Testimonials -->
      <section class="py-20 px-6">
        <div class="max-w-4xl mx-auto text-center bg-white/40 backdrop-blur-md border border-white/30 rounded-3xl shadow-xl p-10">
          <h3 class="text-2xl font-bold text-gray-900 mb-8">نظرات خوانندگان</h3>
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6 text-right">
            <div class="bg-white/60 backdrop-blur-sm p-6 rounded-xl border border-white/40 shadow">
              <p class="italic text-gray-700">«این کتاب مفاهیم عمیق را با زبانی ساده منتقل می‌کند. خواندنش را به همه توصیه می‌کنم!»</p>
              <p class="mt-4 text-sm text-gray-500 text-left">— علی رضایی، توسعه‌دهنده ارشد</p>
            </div>
            <div class="bg-white/60 backdrop-blur-sm p-6 rounded-xl border border-white/40 shadow">
              <p class="italic text-gray-700">«سادگی در توسعه نرم‌افزار را بهتر درک کردم. یک راهنمای واقعی!»</p>
              <p class="mt-4 text-sm text-gray-500 text-left">— سارا محمودی، معمار نرم‌افزار</p>
            </div>
          </div>
        </div>
      </section>

      <!-- FAQ -->
      <section class="py-20 px-6">
        <div class="max-w-4xl mx-auto bg-white/40 backdrop-blur-md rounded-2xl p-10 border border-white/30 shadow-md text-right">
          <h3 class="text-2xl font-bold mb-8 text-center text-gray-900">سوالات متداول</h3>
          <div class="space-y-6 text-gray-700 leading-loose">
            <div>
              <h4 class="font-bold mb-1">این کتاب برای چه کسانی مناسب است؟</h4>
              <p>برای تمام سطوح برنامه‌نویسان و معماران نرم‌افزار</p>
            </div>
            <div>
              <h4 class="font-bold mb-1">آیا مطالعه‌ی کتاب نیاز به تجربه زیاد دارد؟</h4>
              <p>خیر، مطالب برای همه قابل درک هستند</p>
            </div>
            <div>
              <h4 class="font-bold mb-1">آیا نسخه دیجیتال دارد؟</h4>
              <p>بله، در طاقچه و فراکتاب موجود است</p>
            </div>
          </div>
        </div>
      </section>

      <!-- About Translator -->
      <section class="py-20 px-6">
        <div class="max-w-4xl mx-auto text-center bg-white/40 backdrop-blur-md p-10 rounded-2xl border border-white/30 shadow-md">
          <h3 class="text-2xl font-bold mb-4 text-gray-900">درباره مترجم</h3>
          <p class="text-lg font-medium text-gray-800 mb-2">مسلم دریس جرفی</p>
          <p class="text-sm text-gray-600">برنامه‌نویس و مترجم علاقه‌مند به سادگی در طراحی نرم‌افزار</p>
        </div>
      </section>

      <!-- Footer -->
      <footer class="text-center text-sm text-gray-500 py-8 relative z-10">
        &copy; {{ new Date().getFullYear() }} مسلم دریس جرفی. تمامی حقوق محفوظ است.
      </footer>

    </div>
  </div>
</template>

<script>
export default {
  name: 'LandingPage',
  data() {
    return {
      purchaseLinks: {
        'خرید از دیجی‌کالا': 'https://www.digikala.com/product/dkp-18606281/',
        'سایت انتشارات': 'https://www.motekhassesan.com/?p=52527',
        'طاقچه': 'https://taaghche.com/book/226467/سادگی-کد',
        'فراکتاب': 'https://www.faraketab.ir/book/514866-سادگی-کد'
      }
    }
  }
}
</script>

<style scoped>
body {
  font-family: 'Vazirmatn', sans-serif;
}
@keyframes pulse {
  0%, 100% { transform: scale(1); }
  50% { transform: scale(1.05); }
}
.animate-pulse {
  animation: pulse 6s infinite;
}
.delay-200 { animation-delay: 0.2s; }
.delay-300 { animation-delay: 0.3s; }
.delay-500 { animation-delay: 0.5s; }
.delay-[700ms] { animation-delay: 0.7s; }
</style>
