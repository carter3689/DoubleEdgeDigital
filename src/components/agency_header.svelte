<script>
    import { onMount } from 'svelte';

    let burger;
    console.log(burger)
// Burger menus
onMount( () => {
    if (document.readyState !== 'loading') {
                // open
                burger = document.querySelectorAll('.navbar-burger');
        console.log(`inside of ONMONUT: ${burger} `)
        const menu = document.querySelectorAll('.navbar-menu');
    
        if (burger.length && menu.length) {
            for (var i = 0; i < burger.length; i++) {
                burger[i].addEventListener('click', function() {
                    for (var j = 0; j < menu.length; j++) {
                        menu[j].classList.toggle('hidden');
                    }
                });
            }
        }
    
        // close
        const close = document.querySelectorAll('.navbar-close');
        const backdrop = document.querySelectorAll('.navbar-backdrop');
    
        if (close.length) {
            for (var i = 0; i < close.length; i++) {
                close[i].addEventListener('click', function() {
                    for (var j = 0; j < menu.length; j++) {
                        menu[j].classList.toggle('hidden');
                    }
                });
            }
        }
    
        if (backdrop.length) {
            for (var i = 0; i < backdrop.length; i++) {
                backdrop[i].addEventListener('click', function() {
                    for (var j = 0; j < menu.length; j++) {
                        menu[j].classList.toggle('hidden');
                    }
                });
            }
        }
    console.log('document is already ready, just execute code here');
} else {
    document.addEventListener('DOMContentLoaded', function() {

    });
}})
</script>

<section class="relative bg-black overflow-hidden"><div class="relative w-2/3 ml-auto">
    <div class="absolute top-0 left-0 -ml-64 rounded-full h-20 md:h-160 w-80 md:w-160">
      <img class="object-contain transform scale-200" src="boldui-assets/elements/shadow-blue-full.svg" alt="shadow-blue"></div>
    <div class="absolute top-1/2 left-0 mt-40 rounded-full h-20 md:h-160 w-80 md:w-160">
      <img class="object-contain transform scale-200" src="boldui-assets/elements/shadow-light-7.svg" alt="shadow-light"></div>
    <div class="absolute top-0 left-0 -mt-40 ml-40 transform -translate-x-1/2 rotate-45 clip-path" style="width: 1000px; height: 1000px;">
      <img class="h-full transform -rotate-45 object-cover" src="https://images.unsplash.com/photo-1510125964506-dc5a14f3ef4e?crop=entropy&amp;cs=tinysrgb&amp;fm=jpg&amp;ixid=MnwzMzIzMzB8MHwxfHNlYXJjaHwyMHx8YWdlbmN5fGVufDB8fHx8MTY1NzIyNDE4OA&amp;ixlib=rb-1.2.1&amp;q=80&amp;w=1920" alt="background"></div>
    </div>
    <nav class="relative flex mb-24 lg:mb-40 px-16 justify-between bg-transparent border-b"><div class="pr-14 py-8 lg:border-r">
      <a class="inline-block text-xl text-white font-medium font-heading" href="/">
        <h4>DoubleEdge Digital</h4>
      </a>
      </div>
      <div class="hidden lg:block py-8 lg:absolute lg:top-1/2 lg:left-1/2 lg:transform lg:-translate-y-1/2 lg:-translate-x-1/2">
        <ul class="flex justify-center"><li class="mr-6 ml-20"><a class="text-white hover:text-amber-700" href="/agency">Agency</a></li>
          <li class="mr-6"><a class="text-white hover:text-amber-700" href="/courses">Courses</a></li>
          <li><a class="text-white hover:text-amber-700 mr-4" href="/seo-agency">SEO</a></li>
          <li><a class="text-white hover:text-amber-700 mr-4" href="/conversion-agency">CRO</a></li>
          <li><a class="text-white hover:text-amber-700 mr-4" href="/ppc-management-agency">Google</a></li>
          <li><a class="text-white hover:text-amber-700 mr-4" href="/landing-page-agency">Landing</a></li>
          <li><a class="text-white hover:text-amber-700 mr-4" href="/facebook-agency">Facebook</a></li>
          <li><a class="text-white hover:text-amber-700" href="/about-us">About</a></li>
        </ul></div>
      <button class="navbar-burger lg:hidden self-center">
        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><rect y="6" width="24" height="2" fill="white"></rect><rect y="11" width="24" height="2" fill="white"></rect><rect y="16" width="24" height="2" fill="white"></rect></svg></button>
      <div class="hidden lg:flex items-center pl-16 py-8 border-l">
        <div class="flex items-center">
          <a class="inline-block text-sm text-white hover:underline font-heading" href="tel:708-866-1333">(708) 866-1333</a>
        </div>
      </div>
    </nav><div class="relative container mx-auto px-4 pb-24 lg:pb-64">
    <div class="flex flex-wrap -mx-4">
      <div class="w-full lg:w-1/2 px-4 mb-8 lg:mb-0">
        <h2 class="md:max-w-md mx-auto text-2xl sm:text-4xl md:text-6xl text-white uppercase font-heading" contenteditable="false">WE GUARANTEE RESULTS OR..</h2>
      </div>
      <div class="w-full lg:w-1/2 px-4">
        <div class="md:max-w-md mx-auto">
          <p class="mb-20 max-w-sm sm:text-xl font-semibold text-white" contenteditable="false">We give you, your money back...seriously!</p>
          <a class="inline-flex justify-center w-full md:w-auto mb-6 lg:mb-0 md:mr-8 items-center py-4 px-6 rounded-full bg-yellow-300 hover:bg-yellow-400 transform duration-200" href="https://form.typeform.com/to/pCZBEDPU">
            <svg class="mr-3" width="16" height="9" viewBox="0 0 16 9" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M12.01 3.16553H0V5.24886H12.01V8.37386L16 4.20719L12.01 0.0405273V3.16553Z" fill="black"></path></svg><span class="text-sm font-heading"> Book a discovery session</span>
          </a>
        </div>
      </div>
    </div>
    </div>
    <div class="hidden navbar-menu fixed top-0 left-0 bottom-0 w-5/6 max-w-sm z-50">
      <div class="navbar-backdrop fixed inset-0 bg-gray-800 opacity-25"></div>
      <nav class="relative flex flex-col py-8 px-10 w-full h-full bg-black border-r overflow-y-auto">
        <a class="inline-block text-xl text-white font-medium font-heading" href="/">
          <h4>DoubleEdge Digital</h4>
        </a>
        <ul class="mb-32"><li class="mb-10">
          <a class="flex items-center" href="/agency">
            <span class="mr-3 text-lg text-white">Agency</span>
            <svg width="16" height="9" viewBox="0 0 16 9" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M12.01 3.48047H0V5.57278H12.01V8.71124L16 4.52663L12.01 0.34201V3.48047Z" fill="#FFEC3E"></path></svg></a>
          </li>
          <li class="mb-10">
            <a class="flex items-center" href="/courses">
              <span class="mr-3 text-lg text-white">Courses</span>
              <svg width="16" height="9" viewBox="0 0 16 9" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M12.01 3.48047H0V5.57278H12.01V8.71124L16 4.52663L12.01 0.34201V3.48047Z" fill="#FFEC3E"></path></svg></a>
          </li>
          <li class="mb-10">
            <a class="flex items-center" href="/seo-agency">
              <span class="mr-3 text-lg text-white">SEO</span>
              <svg width="16" height="9" viewBox="0 0 16 9" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M12.01 3.48047H0V5.57278H12.01V8.71124L16 4.52663L12.01 0.34201V3.48047Z" fill="#FFEC3E"></path></svg></a>
          </li>
          <li>
            <a class="flex items-center" href="/conversion-rate-agency">
              <span class="mr-3 text-lg text-white">CRO</span>
              <svg width="16" height="9" viewBox="0 0 16 9" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M12.01 3.48047H0V5.57278H12.01V8.71124L16 4.52663L12.01 0.34201V3.48047Z" fill="#FFEC3E"></path></svg></a>
          </li>
          <li>
            <a class="flex items-center" href="/ppc-management-agency">
              <span class="mr-3 text-lg text-white">Google Ads</span>
              <svg width="16" height="9" viewBox="0 0 16 9" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M12.01 3.48047H0V5.57278H12.01V8.71124L16 4.52663L12.01 0.34201V3.48047Z" fill="#FFEC3E"></path></svg></a>
          </li>
          <li>
            <a class="flex items-center" href="/landing-pages-agency">
              <span class="mr-3 text-lg text-white">Landing Pages</span>
              <svg width="16" height="9" viewBox="0 0 16 9" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M12.01 3.48047H0V5.57278H12.01V8.71124L16 4.52663L12.01 0.34201V3.48047Z" fill="#FFEC3E"></path></svg></a>
          </li>
          <li>
            <a class="flex items-center" href="/facebook-agency">
              <span class="mr-3 text-lg text-white">Facebook</span>
              <svg width="16" height="9" viewBox="0 0 16 9" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M12.01 3.48047H0V5.57278H12.01V8.71124L16 4.52663L12.01 0.34201V3.48047Z" fill="#FFEC3E"></path></svg></a>
          </li>
          <li>
            <a class="flex items-center" href="/about-us">
              <span class="mr-3 text-lg text-white">About Us</span>
              <svg width="16" height="9" viewBox="0 0 16 9" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M12.01 3.48047H0V5.57278H12.01V8.71124L16 4.52663L12.01 0.34201V3.48047Z" fill="#FFEC3E"></path></svg></a>
          </li>
        </ul><p class="text-sm text-gray-500">All rights reserved © BoldUI 2021</p>
      </nav></div>
  </section>