<template>
   <!-- Mobile navigation -->
    <nav class="md:hidden bg-gray-900 text-2xl shadow-xl">
        <div class="container mx-auto px-6">
            <div class="flex items-center justify-between py-5">
                <!-- Logo -->
                <a  class="flex justify-center items-center w-14 h-14 bg-white rounded-full">
                    <img src="@/assets/img/near_logo_stack2.png" alt="" class="">
                </a>

                <!-- Buttons -->
                <div class="flex items-center space-x-4">
                    <!-- Logout -->
                    <button @click="signOut" class="text-white">
                        <svg xmlns="http://www.w3.org/2000/svg" width="45" height="45" viewBox="0 0 45 45" fill="none">
                            <path d="M35.625 39.375H18.75C16.6789 39.375 15 37.6961 15 35.625V28.125H18.75V35.625H35.625V9.375H18.75V16.875H15V9.375C15 7.30393 16.6789 5.625 18.75 5.625H35.625C37.6961 5.625 39.375 7.30393 39.375 9.375V35.625C39.375 37.6961 37.6961 39.375 35.625 39.375ZM22.5 30V24.375H5.625V20.625H22.5V15L31.875 22.5L22.5 30Z" fill="currentColor"/>
                        </svg>
                    </button>

                    <!-- Menu -->
                    <a href="" class="text-white">
                        <svg xmlns="http://www.w3.org/2000/svg" width="45" height="45" viewBox="0 0 45 45" fill="none">
                            <path fill-rule="evenodd" clip-rule="evenodd" d="M7.73438 5.625C6.5694 5.625 5.625 6.5694 5.625 7.73438V18.9844C5.625 20.1493 6.5694 21.0938 7.73438 21.0938H18.9844C20.1493 21.0938 21.0938 20.1494 21.0938 18.9844V7.73438C21.0938 6.5694 20.1494 5.625 18.9844 5.625H7.73438ZM8.4375 18.2812V8.4375H18.2812V18.2812H8.4375Z" fill="currentColor"/>
                            <path fill-rule="evenodd" clip-rule="evenodd" d="M26.0156 5.625C24.8507 5.625 23.9062 6.5694 23.9062 7.73438V18.9844C23.9062 20.1493 24.8506 21.0938 26.0156 21.0938H37.2656C38.4306 21.0938 39.375 20.1494 39.375 18.9844V7.73438C39.375 6.5694 38.4306 5.625 37.2656 5.625H26.0156ZM26.7188 18.2812V8.4375H36.5625V18.2812H26.7188Z" fill="currentColor"/>
                            <path fill-rule="evenodd" clip-rule="evenodd" d="M5.625 26.0156C5.625 24.8506 6.5694 23.9062 7.73438 23.9062H18.9844C20.1494 23.9062 21.0938 24.8507 21.0938 26.0156V37.2656C21.0938 38.4306 20.1493 39.375 18.9844 39.375H7.73438C6.5694 39.375 5.625 38.4306 5.625 37.2656V26.0156ZM8.4375 26.7188V36.5625H18.2812V26.7188H8.4375Z" fill="currentColor"/>
                            <path fill-rule="evenodd" clip-rule="evenodd" d="M26.0156 23.9062C24.8507 23.9062 23.9062 24.8506 23.9062 26.0156V37.2656C23.9062 38.4306 24.8506 39.375 26.0156 39.375H37.2656C38.4306 39.375 39.375 38.4306 39.375 37.2656V26.0156C39.375 24.8507 38.4306 23.9062 37.2656 23.9062H26.0156ZM26.7188 36.5625V26.7188H36.5625V36.5625H26.7188Z" fill="currentColor"/>
                        </svg>
                    </a>
                </div>
            </div>
        </div>
    </nav>


    <div class="flex">
        
        <!-- Left side -->
        <div class="hidden md:block sticky top-0 h-screen profile-info bg-gray-900 py-10 xl:py-0 xl:pt-10 ">

            <img src="@/assets/img/pixel-hor.png" alt="" class="absolute h-full top-0 -right-6 ">

            <div class="flex flex-col items-center justify-between h-full">

                <div class="flex flex-col items-center space-y-4 xl:space-y-14">
                    
                    <!-- Mail logo -->
                    <a href="./index.html" class="hidden xl:flex items-center text-white text-5xl font-bold ">
                        <img src="@/assets/img/near_logo_stack1.png" alt="" class="">
                        <span class="h-14 w-0.5 bg-white rounded-full ml-1 mr-3"></span>
                        Mail
                        <img src="@/assets/img/plane-blue.png" alt="" class=" ml-2 -mt-8">
                    </a>

                    <!-- Logo -->
                    <div class="flex flex-col items-center">
                        <a href="#" class="flex justify-center items-center w-14 xl:w-24 h-14 xl:h-24 bg-white rounded-full">
                            <img src="@/assets/img/near_logo_stack2.png" alt="" class="w-10">
                        </a>
                        <p class="hidden xl:block mt-5 text-white text-2xl font-bold">{{accountId}}</p>
                    </div>

                    <!-- Menu -->
                    <a class="xl:hidden text-white">
                        <svg xmlns="http://www.w3.org/2000/svg" width="45" height="45" viewBox="0 0 45 45" fill="none">
                            <path fill-rule="evenodd" clip-rule="evenodd" d="M7.73438 5.625C6.5694 5.625 5.625 6.5694 5.625 7.73438V18.9844C5.625 20.1493 6.5694 21.0938 7.73438 21.0938H18.9844C20.1493 21.0938 21.0938 20.1494 21.0938 18.9844V7.73438C21.0938 6.5694 20.1494 5.625 18.9844 5.625H7.73438ZM8.4375 18.2812V8.4375H18.2812V18.2812H8.4375Z" fill="currentColor"/>
                            <path fill-rule="evenodd" clip-rule="evenodd" d="M26.0156 5.625C24.8507 5.625 23.9062 6.5694 23.9062 7.73438V18.9844C23.9062 20.1493 24.8506 21.0938 26.0156 21.0938H37.2656C38.4306 21.0938 39.375 20.1494 39.375 18.9844V7.73438C39.375 6.5694 38.4306 5.625 37.2656 5.625H26.0156ZM26.7188 18.2812V8.4375H36.5625V18.2812H26.7188Z" fill="currentColor"/>
                            <path fill-rule="evenodd" clip-rule="evenodd" d="M5.625 26.0156C5.625 24.8506 6.5694 23.9062 7.73438 23.9062H18.9844C20.1494 23.9062 21.0938 24.8507 21.0938 26.0156V37.2656C21.0938 38.4306 20.1493 39.375 18.9844 39.375H7.73438C6.5694 39.375 5.625 38.4306 5.625 37.2656V26.0156ZM8.4375 26.7188V36.5625H18.2812V26.7188H8.4375Z" fill="currentColor"/>
                            <path fill-rule="evenodd" clip-rule="evenodd" d="M26.0156 23.9062C24.8507 23.9062 23.9062 24.8506 23.9062 26.0156V37.2656C23.9062 38.4306 24.8506 39.375 26.0156 39.375H37.2656C38.4306 39.375 39.375 38.4306 39.375 37.2656V26.0156C39.375 24.8507 38.4306 23.9062 37.2656 23.9062H26.0156ZM26.7188 36.5625V26.7188H36.5625V36.5625H26.7188Z" fill="currentColor"/>
                        </svg>
                    </a>

                </div>
                <div class="flex flex-col items-center">
                    <!-- Logout -->
                    <button @click="signOut" class="flex items-center text-white hover:text-red-600 -ml-3 transform active:scale-95 duration-100">
                        <svg xmlns="http://www.w3.org/2000/svg" class="w-10 xl:w-7  mr-2" viewBox="0 0 45 45" fill="none">
                            <path d="M35.625 39.375H18.75C16.6789 39.375 15 37.6961 15 35.625V28.125H18.75V35.625H35.625V9.375H18.75V16.875H15V9.375C15 7.30393 16.6789 5.625 18.75 5.625H35.625C37.6961 5.625 39.375 7.30393 39.375 9.375V35.625C39.375 37.6961 37.6961 39.375 35.625 39.375ZM22.5 30V24.375H5.625V20.625H22.5V15L31.875 22.5L22.5 30Z" fill="currentColor"/>
                        </svg>
                        <span class="hidden xl:block">Logout</span>
                    </button>
                    <img src="@/assets/img/lady-employee-working-in-office.png" alt="" class="w-full hidden xl:block">
                </div>
            </div>
        </div>

        <!-- Right side -->
        <div class="w-full h-screen overflow-y-scroll">
            <div class="px-6 xl:px-10">
                
                <!-- Search from - Messaginig btn -->
                <form action="" class="flex flex-col md:flex-row items-center w-full mt-6 lg:mt-10">
                    <!-- Search -->
                    <!-- <input type="text" placeholder="Search or type mail" class="relative search md:mr-24 py-3 outline-none border focus:border-blue-400 w-full rounded-full pl-8"> -->
                    
                    <!-- Start messaginig -->
                    <button @click="modalOpen=true" class="mt-6 md:mt-0 messaging-btn py-4 bg-gradient-to-r from-black to-black hover:from-blue-400 hover:to-blue-300 font-bold text-sm text-white text-center rounded-full transform active:scale-95 duration-150">
                        START MESSAGING
                    </button>

                </form>

                
                <div class="mt-9 xl:mt-11 flex items-center text-gray-400 text-lg">
                    <div class="w-1/5 text-center hidden md:inline-block">date</div>
                    <div class="inline-block w-full md:w-1/5 text-center">sender</div>
                    <div class="inline-block w-full md:w-1/5 text-center">receiver</div>
                    <div class="w-1/6 text-right hidden md:inline-block">
                            <button @click="deleteAllMessages" class="inline-block align-middle text-red-600 transform active:scale-95 duration-100">
                                delete all
                                <svg xmlns="http://www.w3.org/2000/svg" class="float-right mt-1 ml-1" width="12" height="14" viewBox="0 0 12 14" fill="none">
                                    <path fill-rule="evenodd" clip-rule="evenodd" d="M4.875 1.375C4.56434 1.375 4.3125 1.62684 4.3125 1.9375H7.6875C7.6875 1.62684 7.43566 1.375 7.125 1.375H4.875ZM8.8125 1.9375C8.8125 1.00552 8.05698 0.25 7.125 0.25H4.875C3.94302 0.25 3.1875 1.00552 3.1875 1.9375H0.9375C0.62684 1.9375 0.375 2.18934 0.375 2.5C0.375 2.81066 0.62684 3.0625 0.9375 3.0625H11.0625C11.3732 3.0625 11.625 2.81066 11.625 2.5C11.625 2.18934 11.3732 1.9375 11.0625 1.9375H8.8125Z" fill="currentColor"/>
                                    <path fill-rule="evenodd" clip-rule="evenodd" d="M4.55777 5.87615C4.86779 5.85628 5.13522 6.09149 5.1551 6.40151L5.43635 10.789C5.45622 11.099 5.22101 11.3665 4.91098 11.3863C4.60096 11.4062 4.33353 11.171 4.31365 10.861L4.0324 6.47348C4.01253 6.16346 4.24774 5.89602 4.55777 5.87615Z" fill="currentColor"/>
                                    <path fill-rule="evenodd" clip-rule="evenodd" d="M7.44223 5.87615C7.13221 5.85628 6.86477 6.09149 6.8449 6.40151L6.56365 10.789C6.54378 11.099 6.77899 11.3665 7.08902 11.3863C7.39904 11.4062 7.66647 11.171 7.68635 10.861L7.9676 6.47348C7.98747 6.16346 7.75226 5.89602 7.44223 5.87615Z" fill="currentColor"/>
                                    <path fill-rule="evenodd" clip-rule="evenodd" d="M0.981361 4.5734C0.918411 4.06981 1.31108 3.625 1.81859 3.625H10.1814C10.6889 3.625 11.0816 4.06981 11.0186 4.5734L10.0563 12.2718C9.95078 13.1163 9.23291 13.75 8.38187 13.75H3.61813C2.76708 13.75 2.04922 13.1163 1.94366 12.2718L0.981361 4.5734ZM2.13719 4.75L3.05997 12.1323C3.09516 12.4138 3.33445 12.625 3.61813 12.625H8.38187C8.66555 12.625 8.90484 12.4138 8.94003 12.1323L9.86281 4.75H2.13719Z" fill="currentColor"/>
                                </svg>
                            </button>
                        </div>
                </div>
            </div>

            <!-- Message section -->
            <section v-if="myMessages.length>0" class="w-full mt-5 border-t">
                
                <!-- One message -->
                <div v-for="message in myMessages" :key="message"  class="w-full border-b px-6 xl:px-10 py-4 pb-6">

                    <div class=" flex items-center text-sm">
                        <div class="w-1/5 text-center hidden md:inline-block"> {{
                                        format(
                                            new Date(
                                            fromUnixTime(
                                            parseInt(message.timestamp.substring(0, 10))
                                            )
                                        ),
                                        "MMM do yyyy"
                                        )
                                        }}</div>
                        <div class="inline-block w-full md:w-1/5 text-center">{{message.sender}}</div>
                        <div class="inline-block w-full md:w-1/5 text-center">{{accountId}}</div>
                    </div>

                    <p class="text-sm w-full md:w-4/5 mt-5">
                        {{message.message}}
                    </p>
                </div>
            </section>

             <section v-else class="w-full mt-5 border-t">
                
                <img src="@/assets/img/man-listening-music-2194229-0.png" alt="" class="mx-auto">
                <div class="flex justify-center mt-10">
                    <!-- Mail logo -->
                    <a href="./index.html" class="flex items-center text-black text-5xl font-bold ">
                        <img src="@/assets/img/near_logo_stack.png" alt="" class="">
                        <span class="h-14 w-0.5 bg-black rounded-full ml-1 mr-3"></span>
                        Mail
                        <img src="@/assets/img/plane-blue.png" alt="" class=" ml-2 -mt-8">
                    </a>
                </div>
                <p class="text-center mt-4">© 2021 NEAR Ltd</p>
            </section>
        </div>
    </div>

      <loading v-model:active="isLoading"
                 :can-cancel="false"
                 :is-full-page="true"/>

    <TransitionRoot as="template" :show="modalOpen">
        <Dialog as="div" class="fixed z-10 inset-0 overflow-y-auto" @close="modalOpen = false">
            <div class="flex items-end justify-center min-h-screen pt-4 px-4 pb-20 text-center sm:block sm:p-0">
                <TransitionChild as="template" enter="ease-out duration-300" enter-from="opacity-0" enter-to="opacity-100" leave="ease-in duration-200" leave-from="opacity-100" leave-to="opacity-0">
                    <DialogOverlay class="fixed inset-0 bg-gray-500 bg-opacity-75 transition-opacity" />
                        </TransitionChild>

        <!-- This element is to trick the browser into centering the modal contents. -->
        <span class="hidden sm:inline-block sm:align-middle sm:h-screen" aria-hidden="true">&#8203;</span>
        <TransitionChild as="template" enter="ease-out duration-300" enter-from="opacity-0 translate-y-4 sm:translate-y-0 sm:scale-95" enter-to="opacity-100 translate-y-0 sm:scale-100" leave="ease-in duration-200" leave-from="opacity-100 translate-y-0 sm:scale-100" leave-to="opacity-0 translate-y-4 sm:translate-y-0 sm:scale-95">
          <div class="fixed top-0  w-full h-screen bg-50 z-50">
        <div class="flex h-full items-center justify-center">
            <div class="w-11/12 md:w-2/3 xl:w-1/3 bg-white rounded-t-2xl">

                <div class="flex justify-between bg-gray-900 items-center px-6 rounded-t-xl text-white py-3">
                    <p class="">New message</p>
                    <button @click="modalOpen=false" class="hover:text-blue-300 transform active:scale-95 duration-100">
                        <svg xmlns="http://www.w3.org/2000/svg" width="10" height="10" viewBox="0 0 10 10" fill="none">
                            <path d="M1.66667 0L0 1.66667L3.33333 5L0 8.33333L1.66667 10L5 6.66667L8.33333 10L10 8.33333L6.66667 5L10 1.66667L8.33333 0L5 3.33333L1.66667 0Z" fill="currentColor" fill-opacity="0.6"/>
                        </svg>
                    </button>
                </div>

                <form action="" class="mt-2 px-6">
                    <input type="text" placeholder="Recipient" v-model="recipient" class="w-full outline-none border-b pl-6 py-2 font-medium">
                    <textarea v-model="messageBody" cols="30" rows="10" class="w-full pl-6 py-2 outline-none " placeholder="Message body "></textarea>

                    <button @click="handleSubmit" class="inline-block text-white rounded-full my-9 bg-gray-900 font-bold text-sm py-3 px-10 transform active:scale-95 duration-100">SEND</button>
                </form>

                <img src="@/assets/img/pixel.png" alt="" class="w-full">

            </div>
        </div>
    </div>
        </TransitionChild>
      </div>
    </Dialog>
  </TransitionRoot>
</template>

<script>
import Loading from 'vue-loading-overlay';
import 'vue-loading-overlay/dist/vue-loading.css';
import store from '../store/store.js'
import router from '@/router/index.js'
import { useMessageBox } from "@/composables/near"
import { wallet} from "@/services/near";
import { format, fromUnixTime } from "date-fns";
import { ref } from 'vue'
import { Dialog, DialogOverlay, TransitionChild, TransitionRoot } from '@headlessui/vue'

export default {
    components: {
        Loading,
        Dialog,
        DialogOverlay,
        TransitionChild,
        TransitionRoot
    },
    setup() {
         const modalOpen = ref(false)
         const recipient = ref("")
         const messageBody = ref("")
         const accountId  = store.state.accountId;
         const {isLoading, myMessages, deleteAllMessages, sendMessage} = useMessageBox();

         const handleSubmit = () => {
        sendMessage({
          target_account_id:recipient.value,
          message: messageBody.value
        })
         }

         return {
             modalOpen,
             recipient,
             messageBody,
             isLoading,
             myMessages,
             deleteAllMessages,
             sendMessage,
             handleSubmit,
             accountId,
             signOut: () => {
                wallet.signOut();
                localStorage.removeItem(`near-api-js:keystore:${accountId}:testnet`);
                router.push('/')
            },
            format,
            fromUnixTime
         }
    }
}
</script>