<template>
    <div>
        <nav class="bg-blue-400 shadow">
            <div class="max-w-7xl mx-auto px-2 sm:px-6 lg:px-8">
                <div class="relative flex items-center justify-between h-16">
                    <div class="absolute inset-y-0 left-0 flex items-center sm:hidden">
                        <!-- Mobile menu button-->
                        <button id="mobile-menu-button" ref="mobileMenuButton" type="button"
                            class="inline-flex items-center justify-center p-2 rounded-md text-gray-600 hover:text-white hover:bg-gray-700 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-white"
                            aria-controls="mobile-menu" aria-expanded="false">
                            <span class="sr-only">Open main menu</span>
                            <!-- Icon when menu is closed. -->
                            <svg class="block h-6 w-6" xmlns="http://www.w3.org/2000/svg" fill="none"
                                viewBox="0 0 24 24" stroke="currentColor" aria-hidden="true">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M4 6h16M4 12h16M4 18h16" />
                            </svg>
                            <!-- Icon when menu is open. -->
                            <svg class="hidden h-6 w-6" xmlns="http://www.w3.org/2000/svg" fill="none"
                                viewBox="0 0 24 24" stroke="currentColor" aria-hidden="true">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M6 18L18 6M6 6l12 12" />
                            </svg>
                        </button>
                    </div>
                    <div class="flex-1 flex items-center justify-center sm:items-stretch sm:justify-start">
                        <div class="flex-shrink-0 mt-1">
                            <a href="#" class="text-xl font-bold">Brand</a>
                        </div>
                        <div class="hidden sm:block sm:ml-6">
                            <div class="flex space-x-4">
                                <RouterLink to="/"
                                    exactActiveClass="bg-gray-200"
                                    class="text-gray-900 px-3 py-2 rounded-md text-sm font-medium hover:bg-gray-200">Home</RouterLink>
                                <RouterLink to="Contact"
                                    exactActiveClass="bg-gray-200"
                                    class="text-gray-900 px-3 py-2 rounded-md text-sm font-medium hover:bg-gray-200">Contact</RouterLink>
                            </div>
                        </div>
                    </div>
                    <div
                        class="absolute inset-y-0 right-0 flex items-center pr-2 sm:static sm:inset-auto sm:ml-6 sm:pr-0">
                        <div class="relative dropdown">
                            <button type="button"
                                class="bg-white rounded-full flex text-sm focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-offset-gray-800 focus:ring-white"
                                id="user-menu-button" ref="userMenuButton" aria-expanded="false" aria-haspopup="true">
                                <span class="sr-only">Open user menu</span>
                                <img class="h-8 w-8 rounded-full" src="https://via.placeholder.com/150" alt="">
                            </button>
                            <!-- Dropdown menu -->
                            <div class="origin-top-right absolute right-0 mt-2 w-48 rounded-md shadow-lg py-1 bg-white ring-1 ring-black ring-opacity-5 focus:outline-none dropdown-content hidden"
                                role="menu" aria-orientation="vertical" ref="dropdownContent"
                                aria-labelledby="user-menu-button" tabindex="-1">
                                <a href="#" class="block px-4 py-2 text-sm text-gray-700" role="menuitem">Logout</a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Mobile menu, show/hide based on menu state. -->
            <div class="hidden sm:hidden" ref="mobileMenu" id="mobile-menu">
                <div class="px-2 pt-2 pb-3 space-y-1">
                    <a href="#"
                        class="text-gray-900 block px-3 py-2 rounded-md text-base font-medium hover:bg-gray-200">Home</a>
                    <a href="#"
                        class="text-gray-900 block px-3 py-2 rounded-md text-base font-medium hover:bg-gray-200">Contact</a>
                </div>
            </div>
        </nav>
    </div>
</template>