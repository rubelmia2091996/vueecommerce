<template>
    <div class="antialiased bg-gray-50 dark:bg-gray-900">
        <!-- navber start -->
        <Navbar />
        <!-- navber end -->
        <!-- start Sidebar -->
        <Sidebar />
        <!-- end Sidebar -->
        <main class="p-4 md:ml-64 h-auto pt-20">
            <slot />
        </main>
    </div>
</template>
<script setup>
import { onMounted } from 'vue'
import { initFlowbite } from 'flowbite'
import Navbar from './Navbar.vue';
import Sidebar from './Sidebar.vue';
import Footer from './Footer.vue';


// initialize components based on data attribute selectors
onMounted(() => {
    initFlowbite();
})
</script>