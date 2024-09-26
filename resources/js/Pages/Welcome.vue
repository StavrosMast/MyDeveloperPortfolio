<script setup>
import { Head } from '@inertiajs/vue3';

defineProps({
    canLogin: Boolean,
    canRegister: Boolean,
    laravelVersion: String,
    phpVersion: String,
});
</script>

<template>
    <Head title="Developer Portfolio" />
    <div class="min-h-screen bg-gray-900 text-white">
        <header class="fixed top-0 left-0 right-0 z-50 p-6">
            <nav class="flex justify-between items-center">
                <div class="text-2xl font-bold">SM</div>
                <div class="space-x-6">
                    <a href="#about" class="hover:text-purple-400 transition">About</a>
                    <a href="#projects" class="hover:text-purple-400 transition">Projects</a>
                    <a href="#contact" class="hover:text-purple-400 transition">Contact</a>
                </div>
            </nav>
        </header>

        <main>
            <section id="hero" class="min-h-screen flex items-center justify-center">
                <div class="text-center">
                    <h1 class="text-6xl font-extrabold mb-4">Stavros Mastorakis</h1>
                    <p class="text-2xl text-purple-400 mb-8">Full-Stack Developer</p>
                    <a href="#contact" class="bg-purple-600 hover:bg-purple-700 text-white font-bold py-3 px-6 rounded-full transition">Get in touch</a>
                </div>
            </section>

            <section id="about" class="py-20 bg-gray-800">
                <div class="container mx-auto px-6">
                    <h2 class="text-4xl font-bold mb-8">About Me</h2>
                    <p class="text-xl leading-relaxed">
                        I'm a passionate full-stack developer with expertise in modern web technologies. 
                        My goal is to create beautiful, efficient, and user-friendly applications that solve real-world problems.
                    </p>
                </div>
            </section>

            <section id="projects" class="py-20">
                <div class="container mx-auto px-6">
                    <h2 class="text-4xl font-bold mb-12">Featured Projects</h2>
                    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                        <div v-for="i in 3" :key="i" class="bg-gray-800 rounded-lg overflow-hidden shadow-lg">
                            <img src="https://via.placeholder.com/400x250" alt="Project Image" class="w-full h-48 object-cover">
                            <div class="p-6">
                                <h3 class="text-2xl font-bold mb-2">Project {{ i }}</h3>
                                <p class="text-gray-400 mb-4">A brief description of the project and the technologies used.</p>
                                <a href="#" class="text-purple-400 hover:underline">View Project</a>
                            </div>
                        </div>
                    </div>
                </div>
            </section>

            <section id="contact" class="py-20 bg-gray-800">
                <div class="container mx-auto px-6">
                    <h2 class="text-4xl font-bold mb-8">Get in Touch</h2>
                    <form class="max-w-lg mx-auto">
                        <div class="mb-6">
                            <label for="name" class="block text-sm font-medium mb-2">Name</label>
                            <input type="text" id="name" class="w-full px-3 py-2 bg-gray-700 rounded-md">
                        </div>
                        <div class="mb-6">
                            <label for="email" class="block text-sm font-medium mb-2">Email</label>
                            <input type="email" id="email" class="w-full px-3 py-2 bg-gray-700 rounded-md">
                        </div>
                        <div class="mb-6">
                            <label for="message" class="block text-sm font-medium mb-2">Message</label>
                            <textarea id="message" rows="4" class="w-full px-3 py-2 bg-gray-700 rounded-md"></textarea>
                        </div>
                        <button type="submit" class="bg-purple-600 hover:bg-purple-700 text-white font-bold py-3 px-6 rounded-full transition w-full">Send Message</button>
                    </form>
                </div>
            </section>
        </main>

        <footer class="bg-gray-900 py-6 text-center">
            <p class="text-gray-400">© 2024 Stavros Mastorakis. All rights reserved.</p>
        </footer>
    </div>
</template>

<style scoped>
/* Add any additional styles here */
</style>