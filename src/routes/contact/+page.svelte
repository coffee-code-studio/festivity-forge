<script lang="ts">
    import festivityForgeEvent from '$lib/assets/festivity-forge-event.png'
</script>

<img src={festivityForgeEvent} class="hidden md:block w-full h-32 object-cover" alt="Descriptive Alt Text">

<div class="block md:hidden text-rose-800 text-center text-4xl font-semibold py-2 mt-[40px]">
    Contact Us
</div>

<section class="bg-rose-50">
    <div class="py-8 lg:py-16 px-4 mx-auto max-w-screen-md">
        <p class="mb-8 lg:mb-16 font-light text-center text-rose-800 sm:text-xl">Interested in our services? Send us an email to book us for your event</p>
        <form action="#" class="space-y-8">
            <div>
                <label for="email" class="block mb-2 text-sm font-medium text-rose-800">Your email</label>
                <input type="email" id="email" class="shadow-sm bg-rose-800 border border-gray-300 text-rose-50 text-sm rounded-lg focus:ring-primary-500 focus:border-primary-500 block w-full p-2.5" placeholder="email@email.com" required>
            </div>
            <div>
                <label for="subject" class="block mb-2 text-sm font-medium text-rose-800">Subject</label>
                <input type="text" id="subject" class="shadow-sm bg-rose-800 border border-gray-300 text-rose-50 text-sm rounded-lg focus:ring-primary-500 focus:border-primary-500 block w-full p-2.5" placeholder="Let us know how we can help you" required>
            </div>
            <div class="sm:col-span-2">
                <label for="message" class="block mb-2 text-sm font-medium text-rose-800">Your message</label>
                <textarea id="message" rows="6" class="shadow-sm bg-rose-800 border border-gray-300 text-rose-50 text-sm rounded-lg focus:ring-primary-500 focus:border-primary-500 block w-full p-2.5" placeholder="Leave a comment..."></textarea>
            </div>
            <button type="submit" class="py-3 px-5 text-sm font-medium text-center text-rose-50 rounded-lg bg-rose-800 sm:w-fit hover:bg-primary-800 focus:ring-4 focus:outline-none focus:ring-primary-300">Send message</button>
        </form>
    </div>
</section>