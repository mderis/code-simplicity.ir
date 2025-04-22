<template>
  <div dir="rtl" class="bg-white font-sans text-gray-800 tracking-tight overflow-x-hidden">

    <!-- Hero Section -->
    <section class="relative bg-gradient-to-l from-indigo-100 via-purple-50 to-pink-100 pt-24 pb-32 overflow-hidden">
      <!-- Decorative SVG Wave -->
      <svg class="absolute bottom-0 left-0 w-full" viewBox="0 0 1440 320">
        <path fill="#fff" fill-opacity="1"
              d="M0,192L48,202.7C96,213,192,235,288,229.3C384,224,480,192,576,176C672,160,768,160,864,154.7C960,149,1056,139,1152,138.7C1248,139,1344,149,1392,154.7L1440,160L1440,320L1392,320C1344,320,1248,320,1152,320C1056,320,960,320,864,320C768,320,672,320,576,320C480,320,384,320,288,320C192,320,96,320,48,320L0,320Z"/>
      </svg>

      <div class="max-w-6xl mx-auto px-6 md:px-10 relative z-10 flex flex-col lg:flex-row items-center gap-14">

        <!-- Book Info -->
        <div class="text-center lg:text-right flex-1 animate-fade-in">
          <h1 class="text-5xl font-extrabold leading-snug text-gray-900 mb-3">سادگی کد</h1>
          <h2 class="text-xl font-light text-gray-600 mb-6">ترجمه فارسی کتاب Code Simplicity</h2>
          <p class="text-sm text-gray-500 mb-8">نوشته مکس کانات-الکساندر | ترجمه: مسلم دریس جرفی</p>

          <!-- Buttons -->
          <div id="purchase" class="flex flex-wrap justify-center lg:justify-start gap-4">
            <a href="https://www.digikala.com/product/dkp-18606281/" target="_blank"
               class="bg-indigo-600 text-white font-semibold py-2 px-5 rounded-xl shadow-md transition transform hover:scale-105 hover:shadow-lg">
              خرید از دیجی‌کالا
            </a>
            <a href="https://www.motekhassesan.com/?p=52527" target="_blank"
               class="bg-indigo-600 text-white font-semibold py-2 px-5 rounded-xl shadow-md transition transform hover:scale-105 hover:shadow-lg">
              سایت انتشارات
            </a>
            <a href="https://taaghche.com/book/226467/سادگی-کد" target="_blank"
               class="bg-indigo-600 text-white font-semibold py-2 px-5 rounded-xl shadow-md transition transform hover:scale-105 hover:shadow-lg">
              طاقچه
            </a>
            <a href="https://www.faraketab.ir/book/514866-سادگی-کد" target="_blank"
               class="bg-indigo-600 text-white font-semibold py-2 px-5 rounded-xl shadow-md transition transform hover:scale-105 hover:shadow-lg">
              فراکتاب
            </a>
          </div>
        </div>

        <!-- Book Cover -->
        <div class="flex justify-center lg:justify-end animate-fade-in delay-100">
          <div class="glass-frame">
            <img
                src="https://file1.cdn.faraketab.ir/content_file/content-1-514866-1088371/%D8%B3%D8%A7%D8%AF%DA%AF%DB%8C%20%DA%A9%D8%AF.avif"
                alt="جلد کتاب سادگی کد"
                class="w-64 rounded-xl shadow-2xl"
            />
          </div>
        </div>
      </div>
    </section>

    <!-- About the Book -->
    <section id="about" class="py-20 bg-white">
      <div class="max-w-4xl mx-auto px-6 text-justify animate-fade-in">
        <h3 class="text-2xl font-semibold text-center mb-6 text-gray-900">درباره کتاب</h3>
        <div class="bg-white border border-gray-100 shadow-lg rounded-2xl p-8 leading-8 text-gray-700">
          <p>
            کتاب سادگی کد (Code Simplicity) نوشته‌ی مکس کانات-الکساندر، اثری ارزشمند در زمینه‌ی طراحی و توسعه‌ی نرم‌افزار است که به اصول بنیادین سادگی در کدنویسی می‌پردازد. این کتاب با زبانی ساده و مفاهیمی عمیق، به برنامه‌نویسان، معماران نرم‌افزار و مدیران فنی کمک می‌کند تا نرم‌افزارهایی بسازند که پایدار، قابل نگهداری و توسعه‌پذیر باشند...
          </p>
        </div>
      </div>
    </section>

    <!-- About the Translator -->
    <section id="author" class="py-20 bg-gray-50">
      <div class="max-w-4xl mx-auto px-6 text-center animate-fade-in">
        <div class="bg-white border border-gray-200 shadow-md rounded-xl p-8">
          <h3 class="text-2xl font-semibold mb-4 text-gray-900">درباره مترجم</h3>
          <p class="text-lg font-medium mb-2 text-gray-800">مسلم دریس جرفی</p>
          <p class="text-sm text-gray-600">برنامه‌نویس، علاقه‌مند به طراحی نرم‌افزار ساده و قابل نگهداری</p>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <footer class="bg-white border-t border-gray-200 py-6 text-center text-sm text-gray-500">
      &copy; {{ new Date().getFullYear() }} مسلم دریس جرفی. تمامی حقوق محفوظ است.
    </footer>
  </div>
</template>

<script>
export default {
  name: 'LandingPage',
};
</script>

<style scoped>
/* Custom Glass Frame */
.glass-frame {
  background: rgba(255, 255, 255, 0.3);
  backdrop-filter: blur(12px);
  padding: 1rem;
  border-radius: 1.5rem;
  border: 1px solid rgba(255, 255, 255, 0.3);
  box-shadow: 0 15px 40px rgba(0, 0, 0, 0.1);
}

/* Fade-in animation */
@keyframes fadeIn {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

.animate-fade-in {
  animation: fadeIn 1s ease-out both;
}

.delay-100 {
  animation-delay: 0.3s;
}
</style>
