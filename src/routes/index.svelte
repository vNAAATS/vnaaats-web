<script lang="ts">
import { onMount } from "svelte";
 
import * as site from "../typescript/site";

onMount(async () => {
    site.setTitle("Homepage");
    document.body.style.opacity = "0%";

    // Called 300ms after mount
    setTimeout(() => {
        // Do this to hide the messy content organisation that happens at first load
        document.body.style.animation = "0.2s ease-in 0s fadein";
        document.body.style.opacity = "100%";

        //
        document.getElementById("logo")!.style.animation = "0.8s linear 0s translateFromLeft normal";
        document.getElementById("logo-text")!.style.animation = "0.8s linear 0s translateFromRight normal";
        document.getElementById("learn-more")!.style.animation = "0.8s ease-in 0s fadein";
	},300);
    
});
  
</script>

<div class="h-screen scrollbar-none overflow-x-hidden" id="topDiv">
    <div class="flex flex-col items-center justify-center h-full backdrop-filter" style="background-image: url(/banner.jpg); overflow-hidden;">
        <div class="flex flex-col items-center justify-center h-1/3">
        </div>
        <div class="flex flex-col items-center justify-start h-1/3">
            <img src="/vNAAATS.png" class="overflow-hidden select-none" id="logo" width="80%" alt="Logo">
            <div class="text-white font-bitmap text-3xl pt-4 select-none" id="logo-text">
                The Virtual North Atlantic Advanced Air Traffic System
            </div>
            <div class="flex flex-row justify-between mt-10">
                <a href="/fdd" class="border-2 rounded mr-20 px-4 py-2 hover:cursor-pointer scale-100 bg-blue-5 bg-opacity-0 transition duration-500 
                hover:scale-110 hover:bg-opacity-100 font-bitmap font-normal tracking-wider text-lg">
                    Access FDD
                </a>
                <a href="https://discord.gg/7bHtYNuxdx" target="_blank" class="border-2 rounded ml-20 px-4 py-2 hover:cursor-pointer scale-100 bg-discord_purple bg-opacity-0 transition duration-500 
                hover:scale-110 hover:bg-opacity-100 font-bitmap font-normal tracking-wider text-lg">
                    Join the Discord!
                </a>
            </div>
        </div>
        <div class="flex flex-col justify-end items-center h-1/3 font-bitmap font-normal text-2xl">
            <div class="pt-10 select-none" id="learn-more">
                Learn more
            </div>
            <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" 
            class="mb-8 fill-current opacity-10 text-white animate-pulse scale-110 select-none" version="1.1" width="75" height="75" viewBox="0 0 24 24">
            <path d="M7,10L12,15L17,10H7Z" />
        </svg>
        </div>
    </div>
    <div class="flex flex-col h-1/2 justify-evenly overflow-hidden bg-blue-1" >
        <div class="px-12 2xl:pt-8 xl:pt-14 2xl:pb-2 xl:pb-0 text-center 2xl:text-5xl xl:text-4xl font-bitmap font-semibold tracking-wider select-none">
            Revolutionising North Atlantic ATC on the VATSIM Network.
        </div>
        <div class="shadow-5xl p-6 mx-10 2xl:mt-18 xl:mt-6 2xl:mb-10 xl:mb-16" style="background-color: #152C48; border-color: #152C48;">
            <div class="px-12 pt-4 text-center text-3xl font-web font-bold select-none">
                Proudly supported by:
            </div>
            <div class="flex flex-row justify-evenly">
                <div class="flex flex-row justify-center w-1/4">
                    <a href="https://vatsim.net/" class="flex items-center overflow-hidden scale-70 object-contain transition duration-500 hover:scale-80">
                        <img src="/VATSIM_Logo_No_Tagline.png" alt="VATSIM">
                    </a>
                </div>
                <div class="flex flex-row justify-center w-1/4">
                    <a href="https://ganderoceanic.net/" class="flex items-center overflow-hidden scale-70 object-contain transition duration-500 hover:scale-80">
                        <img src="/ZQO_BANNER_TRANSPARENTWHITE.png"  alt="ZQO">
                    </a>
                </div>
                <div class="flex flex-row justify-center w-1/4">
                    <a href="https://vatcan.ca/" class="flex items-top overflow-hidden scale-70 object-contain transition duration-500 hover:scale-80">
                        <img src="/vatcanlogowhite.png" alt="VATCAN">
                    </a>
                </div>
                <div class="flex flex-row justify-end w-1/4">
                    <a href="https://vatsim.uk/" class="flex items-center overflow-hidden scale-70 object-contain transition duration-500 hover:scale-80">
                        <img src="/vatsimuk_whiteblue.png" alt="VATUK">
                    </a>
                </div>
            </div>
        </div>
    </div>
    <div class="flex flex-col h-1/2 justify-start overflow-hidden shadow-5xl" style="background-color: #1A3351;">
        <div class="flex flex-row justify-center w-full">
            <div class="py-8 px-12 text-center 2xl:text-5xl xl:text-4xl font-bitmap font-semibold tracking-widest select-none">
                Features & Toolsets
            </div>
        </div>
        <div class="flex flex-row justify-evenly w-full py-4 font-web font-bold">
            <a href="https://github.com/vNAAATS/vatsim-NAAATS" class="flex flex-row items-center justify-center w-1/3 select-none">
                <div class="flex flex-col scale-100 justify-center w-5/7 items-center 2xl:text-3xl xl:text-2xl shadow-5xl p-6 bg-blue-1 border-2 border-blue-1 rounded select-none
                transition duration-500 hover:scale-105">
                    Oceanic Euroscope Plugin
                    <!-- MD Radar icon -->
                    <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" 
                    width="175" height="175" viewBox="0 0 24 24" class="py-8 fill-current text-white">
                        <path d="M19.07,4.93L17.66,6.34C19.1,7.79 20,9.79 20,12A8,8 0 0,1 12,20A8,8 0 0,1 4,12C4,7.92 7.05,
                        4.56 11,4.07V6.09C8.16,6.57 6,9.03 6,12A6,6 0 0,0 12,18A6,6 0 0,0 18,12C18,10.34 17.33,8.84 16.24,
                        7.76L14.83,9.17C15.55,9.9 16,10.9 16,12A4,4 0 0,1 12,16A4,4 0 0,1 8,12C8,10.14 9.28,8.59 11,8.14V10.28C10.4,
                        10.63 10,11.26 10,12A2,2 0 0,0 12,14A2,2 0 0,0 14,12C14,11.26 13.6,10.62 13,10.28V2H12A10,10 0 0,0 2,
                        12A10,10 0 0,0 12,22A10,10 0 0,0 22,12C22,9.24 20.88,6.74 19.07,4.93Z" />
                    </svg>
                </div> 
            </a>
            <a href="/fdd" class="flex flex-row justify-center items-center w-1/3 scale-100 transition duration-500 hover:scale-110">
                <div class="flex flex-col justify-center items-center w-5/7 p-6 2xl:text-3xl xl:text-2xl  shadow-5xl bg-blue-1 border-2 border-blue-1 rounded">
                    Flight Data Display
                    <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1"
                    width="175" height="175" viewBox="0 0 24 24" class="py-8 fill-current text-white">
                        <path d="M19 12V13.5C21.21 13.5 23 15.29 23 17.5C23 18.32 22.76 19.08 22.33 19.71L21.24 18.62C21.41
                        18.28 21.5 17.9 21.5 17.5C21.5 16.12 20.38 15 19 15V16.5L16.75 14.25L19 12M19 23V21.5C16.79 21.5 15 
                        19.71 15 17.5C15 16.68 15.25 15.92 15.67 15.29L16.76 16.38C16.59 16.72 16.5 17.1 16.5 17.5C16.5 
                        18.88 17.62 20 19 20V18.5L21.25 20.75L19 23M4 3H18C19.11 3 20 3.9 20 5V11L19.5 11C17.66 11 16 11.77 
                        14.81 13H12V17H13L13 17.5C13 18 13.06 18.5 13.17 19H4C2.9 19 2 18.11 2 17V5C2 3.9 2.9 3 4 
                        3M4 7V11H10V7H4M12 7V11H18V7H12M4 13V17H10V13H4Z" />
                    </svg>
                </div>
            </a>
            <a href="/" class="flex flex-row justify-center items-center w-1/3">
                <div class="flex flex-col justify-center w-5/7 items-center 2xl:text-3xl xl:text-2xl shadow-5xl p-6 bg-blue-1 border-2 border-blue-1 rounded select-none">
                    Dedicated Network & API
                    <!-- MD Nework icon -->
                    <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" version="1.1" 
                    width="175" height="175" viewBox="0 0 24 24" class="py-8 fill-current text-white">
                        <path d="M10,2C8.89,2 8,2.89 8,4V7C8,8.11 8.89,9 10,9H11V11H2V13H6V15H5C3.89,15 3,15.89 3,17V20C3,
                        21.11 3.89,22 5,22H9C10.11,22 11,21.11 11,20V17C11,15.89 10.11,15 9,15H8V13H16V15H15C13.89,15 13,15.89 13,
                        17V20C13,21.11 13.89,22 15,22H19C20.11,22 21,21.11 21,20V17C21,15.89 20.11,15 19,15H18V13H22V11H13V9H14C15.11,
                        9 16,8.11 16,7V4C16,2.89 15.11,2 14,2H10M10,4H14V7H10V4M5,17H9V20H5V17M15,17H19V20H15V17Z"/>
                    </svg>
                </div>
            </a>
        </div>
    </div>
    <div class="flex flex-row h-1/14 justify-evenly items-center font-web font-semibold overflow-hidden bg-blue-0" >
        <div class="tracking-wide text-center">
            Copyright © Andrew Ogden 2020-2021. FOR FLIGHT SIMULATION ONLY. NOT TO BE USED FOR REAL WORLD NAVIGATION.
            <br />Learn more about the VATSIM network <a href="https://vatsim.net" class="underline">here</a>.
        </div>
    </div>
</div>