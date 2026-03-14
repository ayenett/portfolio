<template lang="">
    <div class="min-h-screen bg-gradient-to-br from-rose-200 via-pink-100 to-rose-200">

        <Navbar />
        <Hero />
        <Services />
        <About />
    </div>
</template>
<script>

import Aos from 'aos';
import 'aos/dist/aos.css';
import Navbar from './components/Navbar.vue';
import Hero from './components/Hero.vue';
import Services from './components/Services.vue';
import About from './components/About.vue';
import { ref,nextTick,onMounted } from 'vue';

export default {
    components: {
        Navbar,
        Hero,
        Services,
        About
    },
    setup() {
        const loading = ref(true);

        onMounted(async () => {
            await nextTick();

            Aos.init({
                duration: 800,
                easing: 'ease-in-out',
                once: false,
                offset: 100,
            });

            setTimeout(() => {
                loading.value = false;
            }, 800);
        });

        return {
            loading
        };
    }
}
</script>


