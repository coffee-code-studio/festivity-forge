<script lang="ts">
    import festivityEvent from '$lib/assets/festivity-forge-2.png';
</script>

<div class="flex flex-col min-h-screen">
    <!-- Full Page Banner/Header -->
    <header class="w-full flex relative">
        <!-- Left side of the banner - No background image on larger screens -->
        <div class="bg-rose-400 hidden md:flex md:w-1/2 lg:w-1/2 items-center justify-center h-[50vh]">
            <div class="text-center px-4 md:w-3/4 lg:w-3/4 mx-auto">
                <h1 class="text-3xl md:text-4xl lg:text-5xl font-bold text-rose-50 mb-4">Crafting Your Unforgettable Moments with <span class="text-slate-800">Festivity Forge</span></h1>
                <p class="text-lg md:text-xl lg:text-xl font-extrabold text-rose-50 mt-2 mx-auto md:max-w-md lg:max-w-md mb-4">Discover the magic of personalized celebrations and events with our expert team dedicated to making every occasion uniquely memorable.</p>
                <button class="bg-rose-200 hover:bg-slate-800 hover:text-white text-slate-800 font-bold py-2 px-4 rounded mt-4 text-sm md:text-base lg:text-base">
                    <a href="/about">Learn More</a>
                </button>
            </div>
        </div>
        
        <!-- Left side of the banner - Background image on mobile -->
        <div class="md:hidden w-full h-[50vh]">
            <!-- Background image div with opacity -->
            <div class={`absolute top-0 left-0 w-full h-full bg-cover bg-center bg-no-repeat opacity-70 bg-rose-400 ${festivityEvent ? '' : 'hidden'}`}
                 style={`background-image: url(${festivityEvent});`}></div>

            <div class="absolute top-0 left-0 w-full h-full bg-black opacity-40"></div>

            <!-- Text content div -->
            <div class="relative text-center px-4 w-full mx-auto z-10 mt-[65px]">
                <h1 class="text-3xl md:text-4xl lg:text-5xl font-bold text-rose-50 mb-4">Crafting Your Unforgettable Moments at <span class="text-rose-200">Festivity Forge</span></h1>
                <p class="text-lg md:text-xl lg:text-xl font-extrabold text-rose-50 mt-2 mx-auto md:max-w-md lg:max-w-md mb-4">Discover the magic of personalized celebrations and events with our expert team dedicated to making every occasion uniquely memorable.</p>
                <button class="bg-rose-200 hover:bg-slate-800 hover:text-white text-slate-800 font-bold py-2 px-4 rounded mt-4 text-sm md:text-base lg:text-base">
                    Learn More
                </button>
            </div>
        </div>

        <!-- Right side of the banner, hidden on mobile -->
        <div class="bg-white hidden md:flex md:w-1/2 lg:w-1/2 items-center justify-center h-[50vh]">
            <img src={festivityEvent} alt="Festival Event" class="object-cover h-full w-full opacity-70" />
        </div>
    </header>
    
    <!-- Article Sections -->
    <div class="flex-grow grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-3">
        <!-- Article 1 -->
        <div class="bg-amber-400 p-4 rounded flex flex-col justify-center items-center space-y-4 h-[23rem]">
            <div class="text-center">
                <h2 class="font-bold sm:text-4xl mb-4 text-4xl text-amber-50">Weddings</h2>
                <p class="text-amber-900 text-lg font-extrabold max-w-md mb-4">At Festivity Forge, we specialize in crafting unforgettable wedding experiences. Our expert team tailors full-scale event solutions to meet your unique needs, ensuring a memorable and flawless wedding day.</p>
            </div>
            <a href="/weddings">
                <button class="bg-amber-900 hover:bg-white hover:text-slate-800 text-white font-bold py-2 px-4 rounded">
                    Read More
                </button>
            </a>
        </div>

        <!-- Article 2 -->
        <div class="bg-emerald-400 p-4 rounded flex flex-col justify-center items-center space-y-4 h-[23rem]">
            <div class="text-center">
                <h2 class="font-bold sm:text-4xl text-4xl mb-4 text-emerald-50">Nonprofit Events</h2>
                <p class="text-emerald-900 text-lg font-extrabold max-w-md mb-4">For nonprofit events, Festivity Forge excels in transforming venues with creative and custom decor that suits diverse themes and aesthetic preferences. We specialize in making your nonprofit event truly special.</p>
            </div>
            <a href="/non-profit">
                <button class="bg-emerald-900 hover:bg-white hover:text-slate-800 text-white font-bold py-2 px-4 rounded">
                    Read More
                </button>
            </a>
        </div>

        <!-- Article 3 -->
        <div class="bg-sky-400 p-4 rounded flex flex-col justify-center items-center space-y-4 h-[23rem]">
            <div class="text-center">
                <h2 class="font-bold sm:text-4xl text-4xl mb-4 text-sky-50">Social Celebrations</h2>
                <p class="text-sky-900 text-lg font-extrabold max-w-md mb-4">When it comes to social celebrations, we provide professional and seamless event execution. From meticulous planning to flawless day-of coordination, Festivity Forge ensures your social celebration is a success.</p>
            </div>
            <a href="/social-celebrations">
                <button class="bg-sky-900 hover:bg-white hover:text-slate-800 text-white font-bold py-2 px-4 rounded">
                    Read More
                </button>
            </a>
        </div>

        <!-- Article 4 - Contact Information (Visible on iPad sizes, hidden on mobile and normal desktop sizes) hidden md:block lg:hidden -->
        <div class="hidden lg:hidden md:flex bg-purple-400 p-4 rounded flex flex-col justify-center items-center space-y-4 h-[23rem]">
            <div class="text-center">
                <h2 class="font-bold sm:text-4xl text-4xl mb-4 text-purple-50">Contact</h2>
                <p class="text-purple-900 text-lg font-extrabold max-w-md mb-4">Visit our contact page and send us an email to find out more information that is needed to schedule your event with Festivity Forge. We hope that you will strongly consider using our services!</p>
            </div>
            <button class="bg-purple-900 hover:bg-white hover:text-slate-800 text-white font-bold py-2 px-4 rounded">
                <a href="/contact">Contact Us</a>
            </button>
        </div>
    </div>
</div>
