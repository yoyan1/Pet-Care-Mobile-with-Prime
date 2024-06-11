<script setup>
import {ref} from 'vue';

const op = ref();

const OpToggle = (event) => {
    op.value.toggle(event);
}

</script>
<template>
    <section class="bg-gray-50 dark:bg-gray-900">
        <div class="mx-auto max-w-2xl h-[100vh]">
            <div class="flex justify-between items-center p-5 bg-white">
                <i class="pi pi-align-left" style="font-size: 1rem"></i>
                <h1 class="font-bold text-2xl">PET CARE</h1>
                <div class="flex items-center">
                    <div class="flex items-center ms-3">
                        <div>
                            <button type="button" @click="OpToggle"
                                class="flex text-sm bg-gray-800 rounded-full focus:ring-4 focus:ring-green-500 dark:focus:ring-green-600"
                                aria-expanded="false" data-dropdown-toggle="dropdown-user">
                                <span class="sr-only">Open user menu</span>
                                <!-- <img class="w-8 h-8 rounded-full"
                                    src="/def"
                                    alt="user photo"> -->
                                <img class="w-8 h-8 rounded-full"
                                    src="/default.jpg"
                                    alt="user photo">
                            </button>
                        </div>
                        <OverlayPanel ref="op">
                            <div class="text-base list-none bg-white">
                                <div class="px-4 py-3" role="none">
                                    <p class="text-sm text-gray-900 dark:text-white" role="none">
                                        Roland Clarion
                                    </p>
                                    <p class="text-sm font-medium text-gray-900 truncate dark:text-gray-300"
                                        role="none">
                                      sample@gmail.com
                                    </p>
                                </div>
                                <hr>
                                <ul class="py-1" role="none">
                                    <li>
                                        <router-link  to="user-account" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-100 dark:text-gray-300 dark:hover:bg-gray-600 dark:hover:text-white" role="menuitem">Edit profile</router-link>
                                    </li>
                                    <li>
                                        <a class="block cursor-pointer px-4 py-2 text-sm text-gray-700 hover:bg-gray-100 dark:text-gray-300 dark:hover:bg-gray-600 dark:hover:text-white"
                                            role="menuitem">Sign out</a>
                                    </li>
                                </ul>
                            </div>
                        </OverlayPanel>
                    </div>
              </div>
            </div>
            <div class="flex flex-col gap-5 pt-5 pb-3 px-10 bg-white">
                <h1 class="text-2xl font-semibold">Search for a pet</h1>
                <InputText class="bg-gray-100" placeholder="search"/>
                <div class="flex gap-5">
                    <div class="w-12 h-12 flex justify-center items-center rounded-xl bg-gray-100">
                        <font-awesome-icon icon="fa-solid fa-user-secret" />
                    </div>
                    <div class="w-12 h-12 flex justify-center items-center rounded-xl bg-gray-100">
                        <font-awesome-icon icon="fa-solid fa-user-secret" />
                    </div>
                    <div class="w-12 h-12 flex justify-center items-center rounded-xl bg-gray-100">
                        <font-awesome-icon icon="fa-solid fa-user-secret" />
                    </div>
                    <div class="w-12 h-12 flex justify-center items-center rounded-xl bg-gray-100">
                        <font-awesome-icon icon="fa-solid fa-user-secret" />
                    </div>
                </div>
            </div>
            <div class="flex flex-col gap-5 px-10 ">
                <h1>All pets</h1>
                <div>
                    <div class="flex justify-between items-center bg-white p-2 rounded-xl">
                        <div class="flex gap-5">
                            <img src="/dog.jpg" width="100" height="100" alt="">
                            <div>
                                <span>Dog</span><br>
                                <span class="text-gray-400">Owner: roland</span>
                            </div>
                        </div>
                        <div class="w-12 h-12 flex justify-center items-center rounded-xl bg-gray-100">
                            <font-awesome-icon icon="fa-solid fa-user-secret" />
                        </div>
                    </div>
                </div>
            </div>
        </div>
      </section>
</template>