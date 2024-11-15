<template>
    <div class="min-h-screen bg-gray-50">

        <section class="container mx-auto px-6 py-16">
            <div class="flex flex-col md:flex-row-reverse items-center">
                <div class="md:w-1/2 animate-slide-in-left">
                    <img src="https://images.unsplash.com/photo-1731360433657-bf7be6d169a6?q=80&w=2071&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
                        alt="Mentorship" class="rounded-lg shadow-xl" />
                </div>
                <div class="md:w-1/2 md:pl-12 mt-8 md:mt-0 animate-slide-in-right">
                    <h1 class="text-4xl font-bold text-gray-900 mb-4">
                        Connect with Mentors & Organizations
                    </h1>
                    <p class="text-lg text-gray-600 mb-8">
                        Find the perfect mentor to guide your journey or connect with organizations
                        that align with your goals. Start your growth journey today.
                    </p>
                    <div class="space-y-4 md:space-x-4 md:space-y-0">
                        <button
                            class="bg-[#134b70] text-white px-6 py-3 rounded-lg hover:bg-[#134b70] transition-all hover:scale-105">
                            Find a Mentor
                        </button>
                        <button
                            class="border border-teal-600 text-[#134b70] px-6 py-3 rounded-lg hover:bg-teal-50 transition-all hover:scale-105">
                            Become a Mentor
                        </button>
                    </div>
                </div>
            </div>
        </section>


        <section class="bg-white py-16 overflow-hidden">
            <div class="container mx-auto px-6">
                <h2 class="text-3xl font-bold text-center mb-12">Our Sponsors</h2>
                <div class="sponsors-wrapper">
                    <div class="sponsors-track">
                        <template v-for="i in 16" :key="i">
                            <div class="sponsor-item">
                                <img src="https://images.unsplash.com/photo-1731360433657-bf7be6d169a6?q=80&w=2071&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
                                    :alt="'Sponsor ' + ((i - 1) % 8 + 1)" class="w-full h-full rounded-2xl" />
                            </div>
                        </template>
                    </div>
                </div>
            </div>
        </section>


        <section class="bg-[#134b70] text-white py-16">
            <div class="container mx-auto px-6">
                <div class="grid grid-cols-2 md:grid-cols-4 gap-8">
                    <div class="text-center animate-count-up" v-for="stat in statistics" :key="stat.label">
                        <div class="text-4xl font-bold mb-2">{{ stat.value }}</div>
                        <div class="text-teal-100">{{ stat.label }}</div>
                    </div>
                </div>
            </div>
        </section>


        <section class="py-16">
            <div class="container mx-auto px-6">
                <h2 class="text-3xl font-bold text-center mb-12">Top Performing Teams</h2>
                <div class="grid grid-cols-1 md:grid-cols-3 lg:grid-cols-5 gap-6">
                    <div v-for="i in 5" :key="i"
                        class="team-card bg-white rounded-lg shadow-lg p-6 hover:shadow-xl transition-all duration-300"
                        :style="{ animationDelay: `${i * 0.2}s` }">
                        <img src="https://images.unsplash.com/photo-1731360433657-bf7be6d169a6?q=80&w=2071&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
                            :alt="'Team ' + i" class="w-full rounded-lg mb-4" />
                        <h3 class="font-bold text-lg mb-2">Team {{ i }}</h3>
                        <p class="text-gray-600 text-sm mb-4">some description of the team</p>
                        <div class="flex items-center text-sm text-gray-500">
                            <span>{{ 4 + i }} Members</span>
                            <span class="mx-2">•</span>
                            <span>{{ 3 + i }} Skills to learn</span>
                        </div>
                    </div>
                </div>
                <div class="text-center mt-8">
                    <button
                        class="bg-[#134b70] text-white px-8 py-3 rounded-lg hover:bg-[#134b70] transition-all hover:scale-105">
                        Explore More Teams
                    </button>
                </div>
            </div>
        </section>


        <section class="bg-gray-50 py-16">
            <div class="container mx-auto px-6">
                <h2 class="text-3xl font-bold text-center mb-12">Leaderboards</h2>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-8">

                    <div class="leaderboard-card bg-white rounded-lg shadow-lg p-6">
                        <h3 class="font-bold text-xl mb-4">Top Teams</h3>
                        <div v-for="i in 10" :key="i"
                            class="flex items-center py-2 border-b last:border-0 hover:bg-teal-50 transition-colors">
                            <span class="w-8 font-bold">{{ i }}.</span>
                            <span class="flex-grow">Team {{ i }}</span>
                            <span class="text-[#134b70]">{{ 1000 - (i * 50) }} pts</span>
                        </div>
                    </div>


                    <div class="leaderboard-card bg-white rounded-lg shadow-lg p-6" style="animation-delay: 0.2s">
                        <h3 class="font-bold text-xl mb-4">Top Members</h3>
                        <div v-for="i in 10" :key="i"
                            class="flex items-center py-2 border-b last:border-0 hover:bg-teal-50 transition-colors">
                            <span class="w-8 font-bold">{{ i }}.</span>
                            <span class="flex-grow">Member {{ i }}</span>
                            <span class="text-[#134b70]">{{ 800 - (i * 40) }} pts</span>
                        </div>
                    </div>


                    <div class="leaderboard-card bg-white rounded-lg shadow-lg p-6" style="animation-delay: 0.4s">
                        <h3 class="font-bold text-xl mb-4">Top Skills</h3>
                        <div v-for="i in 10" :key="i"
                            class="flex items-center py-2 border-b last:border-0 hover:bg-teal-50 transition-colors">
                            <span class="w-8 font-bold">{{ i }}.</span>
                            <span class="flex-grow">{{ skills[i - 1] }}</span>
                            <span class="text-[#134b70]">{{ 600 - (i * 30) }} users</span>
                        </div>
                    </div>
                </div>
            </div>
        </section>


        <section class="py-16">
            <div class="container mx-auto px-6">
                <h2 class="text-3xl font-bold text-center mb-12">Available Skills</h2>
                <div class="grid grid-cols-2 md:grid-cols-5 gap-4">
                    <div v-for="(skill, index) in skills" :key="skill"
                        class="skill-card bg-white rounded-lg shadow p-6 text-center hover:shadow-lg transition-all hover:scale-105"
                        :style="{ animationDelay: `${index * 0.1}s` }">
                        <div class="flex flex-col items-center gap-3">

                            <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-[#134b70]" viewBox="0 0 24 24"
                                fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"
                                stroke-linejoin="round">
                                <polygon
                                    points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2">
                                </polygon>
                            </svg>
                            <div class="text-[#134b70] text-lg font-medium">{{ skill }}</div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </div>
</template>

<script setup>
import { ref } from 'vue'

const statistics = ref([
    { label: 'Active Users', value: '10,000+' },
    { label: 'Teams', value: '500+' },
    { label: 'Skills', value: '50+' },
    { label: 'Mentors', value: '1,000+' }
])

const skills = ref([
    'Web Development',
    'Mobile Development',
    'Data Science',
    'UI/UX Design',
    'Digital Marketing',
    'Project Management',
    'Machine Learning',
    'Cloud Computing',
    'Cybersecurity',
    'Business Analysis'
])
</script>

<style>
.sponsors-wrapper {
    width: 100%;
    overflow: hidden;
    position: relative;
}

.sponsors-track {
    display: flex;
    gap: 2rem;
    width: max-content;
    animation: infiniteScroll 30s linear infinite;
}

.sponsor-item {
    flex: 0 0 auto;
    width: 128px;
    height: 128px;
}

@keyframes infiniteScroll {
    0% {
        transform: translateX(0);
    }

    100% {
        transform: translateX(calc(-128px * 8 - 2rem * 8));
    }
}


.animate-slide-in-left {
    animation: slideInLeft 1s ease-out;
}

.animate-slide-in-right {
    animation: slideInRight 1s ease-out;
}



.team-card {
    animation: fadeInUp 0.6s ease-out both;
}


.leaderboard-card {
    animation: slideInUp 0.6s ease-out both;
}


.skill-card {
    animation: fadeInScale 0.4s ease-out both;
}


@keyframes slideInLeft {
    from {
        opacity: 0;
        transform: translateX(-100px);
    }

    to {
        opacity: 1;
        transform: translateX(0);
    }
}

@keyframes slideInRight {
    from {
        opacity: 0;
        transform: translateX(100px);
    }

    to {
        opacity: 1;
        transform: translateX(0);
    }
}

@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translateY(20px);
    }

    to {
        opacity: 1;
        transform: translateY(0);
    }
}

@keyframes slideInUp {
    from {
        opacity: 0;
        transform: translateY(40px);
    }

    to {
        opacity: 1;
        transform: translateY(0);
    }
}

@keyframes fadeInScale {
    from {
        opacity: 0;
        transform: scale(0.9);
    }

    to {
        opacity: 1;
        transform: scale(1);
    }
}


.team-card:hover {
    transform: translateY(-5px);
}

.skill-card:hover {
    transform: scale(1.05);
}


.transition-all {
    transition-property: all;
    transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
    transition-duration: 300ms;
}
</style>