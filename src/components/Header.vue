<template>
  <header class="relative w-full lg:h-screen header-bg">

            <!-- Decorative img -->
            <img src="@/assets/img/pixel-xl.png" alt="" class="absolute bottom-0 w-full">

            <!-- Navbar -->
            <div class="w-full border-b bg-white">
                <div class="container mx-auto px-6">
                    
                    <nav class="flex flex-col md:flex-row items-center justify-between py-5 ">
        
                        <!-- Mail logo -->
                        <a href="./index.html" class="flex items-center text-black text-5xl font-bold ">
                            <img src="@/assets/img/near_logo_stack.png" alt="" class="">
                            <span class="h-14 w-0.5 bg-black rounded-full ml-1 mr-3"></span>
                            Mail
                            <img src="@/assets/img/plane-blue.png" alt="" class=" ml-2 -mt-8">
                        </a>
                        
                        <!-- Login buttons -->
                        <div class="flex flex-col-reverse md:flex-row items-center mt-8 md:mt-0">

                            <!-- Login with NEAR -->
                            <button @click="signIn" class="md:ml-8 bg-gradient-to-r from-black to-black hover:from-blue-400 hover:to-blue-300 font-bold text-white rounded-full px-12 py-2 flex items-center transform active:scale-95 duration-100">
                                <img src="@/assets/img/near_logo_stack1.png" alt="" class="w-8 mr-2">
                                Login with NEAR
                            </button>
                        </div>
                    </nav>
                </div>
            </div>

            <!-- Offer -->
            <div class="container mx-auto px-6  ">
                <div class="flex flex-col lg:flex-row">

                    <!-- Left side offer -->
                    <div class="w-full lg:w-1/2 mt-14 lg:mt-24">
                        <h1 class="relative inline-block pl-12 text-4xl md:text-8xl 2xl:text-9xl font-extrabold">
                            NEAR Mail
                            <img src="@/assets/img/plane-xl.png" alt="" class="absolute -right-10 -top-5 lg:-right-24 lg:-top-12 w-8 lg:w-20">
                        </h1>
                        <div class="flex items-center space-x-4 text-sm 2xl:text-xl mt-8">
                            <div class="h-0.5 w-20 2xl:w-24 bg-gradient-to-r from-blue-400 to-blue-300"></div>
                            <p class="font-bold">
                                The contract provide here, enable to send message to other account and recive message from other accounts
                            </p>
                        </div>
                        <div class="flex justify-center mt-12 lg:mt-4 2xl:mt-12">
                            <a href="./dashboard.html" class="bg-gradient-to-r from-black to-black hover:from-blue-400 hover:to-blue-300 text-white font-bold text-base 2xl:text-xl rounded-full px-10 py-3 transform active:scale-95 duration-100">
                                START MESSAGING
                            </a>
                        </div>
                    </div>
                    
                    <!-- Right side offer -->
                    <div class="w-full lg:w-1/2 mt-24">
                        <img src="@/assets/img/mail-img.png" alt="" class="">
                    </div>

                </div>
            </div>
    </header>
</template>

<script>
export default {
    props:{
        signIn: {
            typeof:Function,
            required:true
        }
    }
}
</script>