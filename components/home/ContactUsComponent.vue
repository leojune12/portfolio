<script lang="ts" setup></script>

<template>
    <div class="bg-gray-900" id="contact-us">
        <div class="py-8 lg:py-16 px-4 mx-auto max-w-screen-md">
            <h2 class="mb-4 text-4xl tracking-tight font-extrabold text-center text-white">Contact Us</h2>
            <p class="mb-8 lg:mb-16 font-light text-center text-gray-400 sm:text-xl">Got a technical issue? Want to send feedback about a beta feature? Need details about our Business plan? Let us know.</p>
            <form action="#" class="space-y-8">
                <div>
                    <label for="email" class="block mb-2 text-sm font-medium text-gray-300">Your email</label>
                    <input type="email" id="email" class="shadow-sm border text-sm rounded-lg block w-full p-2.5 bg-gray-700 border-gray-600 placeholder-gray-400 text-white focus:ring-green-500 focus:border-green-500 shadow-sm-light" placeholder="name@flowbite.com" required>
                </div>
                <div>
                    <label for="subject" class="block mb-2 text-sm font-medium text-gray-300">Subject</label>
                    <input type="text" id="subject" class="block p-3 w-full text-sm rounded-lg border shadow-sm bg-gray-700 border-gray-600 placeholder-gray-400 text-white focus:ring-green-500 focus:border-green-500 shadow-sm-light" placeholder="Let us know how we can help you" required>
                </div>
                <div class="sm:col-span-2">
                    <label for="message" class="block mb-2 text-sm font-medium text-gray-400">Your message</label>
                    <textarea id="message" rows="6" class="block p-2.5 w-full text-sm rounded-lg shadow-sm border bg-gray-700 border-gray-600 placeholder-gray-400 text-white focus:ring-green-500 focus:border-green-500" placeholder="Leave a comment..."></textarea>
                </div>
                <button type="submit" class="py-3 px-5 text-sm font-medium text-center text-white rounded-lg sm:w-fit focus:ring-4 focus:outline-none bg-green-600 hover:bg-green-700 focus:ring-green-800">Send message</button>
            </form>
        </div>
    </div>
</template>

<style scoped></style>
