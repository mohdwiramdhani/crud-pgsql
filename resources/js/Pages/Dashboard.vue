<script setup>
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import { Head } from '@inertiajs/vue3';

</script>

<template>
    <Head title="Dashboard" />

    <AuthenticatedLayout>
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">Dashboard</h2>
        </template>

        <div class="py-12">
            <div class="max-w-7xl mx-auto sm:px-6 lg:px-8">
                <div class="grid grid-cols-1 gap-6 sm:grid-cols-2 lg:grid-cols-3">
                    <!-- Card 1 -->
                    <div class="bg-white overflow-hidden shadow-md rounded-lg">
                        <div class="p-6">
                            <h3 class="font-bold text-lg mb-2">Selamat Datang, {{ $page.props.auth.user.name }}!</h3>
                            <p class="text-gray-700">Silahkan lakukan YA.</p>
                        </div>
                    </div>
                    <!-- Card 2 -->
                    <div class="bg-white overflow-hidden shadow-md rounded-lg">
                        <div class="p-6">
                            <h3 class="font-bold text-lg mb-2">Recent Activity</h3>
                            <p class="text-gray-700">Check your latest activities here.</p>
                        </div>
                    </div>
                    <!-- Card 3 -->
                    <div class="bg-white overflow-hidden shadow-md rounded-lg">
                        <div class="p-6">
                            <h3 class="font-bold text-lg mb-2">Notifications</h3>
                            <p class="text-gray-700">You have no new notifications.</p>
                        </div>
                    </div>
                </div>

                <div class="mt-6">
                    <div class="bg-white p-6 shadow-md rounded-lg">
                        <h3 class="font-bold text-lg mb-2">User Statistics</h3>
                        <div class="flex flex-wrap">
                            <div class="w-full sm:w-1/2 lg:w-1/4 p-4">
                                <div class="bg-blue-500 text-white p-4 rounded-lg shadow-md">
                                    <h4 class="text-sm font-semibold">Total Users</h4>
                                    <p class="text-2xl">1,250</p>
                                </div>
                            </div>
                            <div class="w-full sm:w-1/2 lg:w-1/4 p-4">
                                <div class="bg-green-500 text-white p-4 rounded-lg shadow-md">
                                    <h4 class="text-sm font-semibold">Active Users</h4>
                                    <p class="text-2xl">800</p>
                                </div>
                            </div>
                            <div class="w-full sm:w-1/2 lg:w-1/4 p-4">
                                <div class="bg-yellow-500 text-white p-4 rounded-lg shadow-md">
                                    <h4 class="text-sm font-semibold">Pending Approvals</h4>
                                    <p class="text-2xl">30</p>
                                </div>
                            </div>
                            <div class="w-full sm:w-1/2 lg:w-1/4 p-4">
                                <div class="bg-red-500 text-white p-4 rounded-lg shadow-md">
                                    <h4 class="text-sm font-semibold">Banned Users</h4>
                                    <p class="text-2xl">5</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </AuthenticatedLayout>
</template>
