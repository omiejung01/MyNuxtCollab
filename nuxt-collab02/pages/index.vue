<template>
    <!-- <canvas id="myCanvas"></canvas> -->
    <div class="p-10">
        <div id="wavepanel" class="align-bottom p-8 space-y-4 grid grid-cols-7 gap-4 rounded-lg border-4 max-w-5xl container mx-auto">
            <!-- <div class="rounded-lg border-4 col-span-1"> -->
            <img class="object-cover rounded-lg border-4 col-span-1 w-44" src="https://media04.tetraserver.com/uploads/videos/1667730702_Jazz-01-Piano.png"><div class="rounded-lg border-4 col-span-6 align-top h-24 "><div id="waveform01" class="border-0 w-full"></div></div>
            <img class="object-cover rounded-lg border-4 col-span-1 w-44" src="https://media04.tetraserver.com/uploads/videos/1667730837_Jazz-02-Drum.png"><div class="rounded-lg border-4 col-span-6 align-top h-24" ><div id="waveform02" class="border-0 w-full"></div></div>
            <img class="object-cover rounded-lg border-4 col-span-1 w-44" src="https://media04.tetraserver.com/uploads/videos/1667731195_Jazz-03-Saxophone.png"><div class="rounded-lg border-4 col-span-6 align-top h-24"><div id="waveform03" class="border-0 w-full"></div></div>
            <img class="object-cover rounded-lg border-4 col-span-1 w-44" src="https://media04.tetraserver.com/uploads/videos/1667731377_Jazz-04-DoubleBass.png"><div class="rounded-lg border-4 col-span-6 align-top h-24"><div id="waveform04" class="border-0 w-full"></div></div>
       
        </div>
    </div>

</template>

<script setup lang="ts">
import WaveSurfer from 'wavesurfer.js';
import TimelinePlugin from 'wavesurfer.js/dist/plugins/timeline.js';

onMounted(() => {

    // Create a timeline plugin instance with custom options 4 times
    const topTimeline01 = TimelinePlugin.create({
    height: 20,
    insertPosition: 'beforebegin',
    timeInterval: 0.2,
    primaryLabelInterval: 5,
    secondaryLabelInterval: 1,
    style: {
        fontSize: '16px',
        color: '#2D5B88',
    },
    })

    const topTimeline02 = TimelinePlugin.create({
    height: 20,
    insertPosition: 'beforebegin',
    timeInterval: 0.2,
    primaryLabelInterval: 5,
    secondaryLabelInterval: 1,
    style: {
        fontSize: '16px',
        color: '#2D5B88',
    },
    })

    const topTimeline03 = TimelinePlugin.create({
    height: 20,
    insertPosition: 'beforebegin',
    timeInterval: 0.2,
    primaryLabelInterval: 5,
    secondaryLabelInterval: 1,
    style: {
        fontSize: '16px',
        color: '#2D5B88',
    },
    })

    const topTimeline04 = TimelinePlugin.create({
    height: 20,
    insertPosition: 'beforebegin',
    timeInterval: 0.2,
    primaryLabelInterval: 5,
    secondaryLabelInterval: 1,
    style: {
        fontSize: '16px',
        color: '#2D5B88',
    },
    })


    // Create a second timeline
    const bottomTimline = TimelinePlugin.create({
    height: 10,
    timeInterval: 0.1,
    primaryLabelInterval: 1,
    style: {
        fontSize: '10px',
        color: '#6A3274',
    },
    })

    const wavesurfer01 = WaveSurfer.create({
        container: '#waveform01',
    
        waveColor: 'violet',
        height:96,
        progressColor: 'purple',
        // Set a bar width
        barWidth: 2,
        // Optionally, specify the spacing between bars
        barGap: 1,
        // And the bar radius
        barRadius: 2,
        minPxPerSec: 100,
        plugins: [topTimeline01],
        url: '/Jazz-01-Piano_120.mp4',

    })

    const wavesurfer02 = WaveSurfer.create({
        container: '#waveform02',
    
        waveColor: 'violet',
        height:96,
        progressColor: 'purple',
        // Set a bar width
        barWidth: 2,
        // Optionally, specify the spacing between bars
        barGap: 1,
        // And the bar radius
        barRadius: 2,
        minPxPerSec: 100,
        plugins: [topTimeline02],
        url: '/Jazz-02-Drum_120.mp4',

    })

    const wavesurfer03 = WaveSurfer.create({
        container: '#waveform03',
    
        waveColor: 'violet',
        height:96,
        progressColor: 'purple',
        // Set a bar width
        barWidth: 2,
        // Optionally, specify the spacing between bars
        barGap: 1,
        // And the bar radius
        barRadius: 2,
        minPxPerSec: 100,
        plugins: [topTimeline03],
        url: '/Jazz-03-Saxophone_120.mp4',

    })

    const wavesurfer04 = WaveSurfer.create({
        container: '#waveform04',
    
        waveColor: 'violet',
        height:96,
        progressColor: 'purple',
        // Set a bar width
        barWidth: 2,
        // Optionally, specify the spacing between bars
        barGap: 1,
        // And the bar radius
        barRadius: 2,
        minPxPerSec: 100,
        plugins: [topTimeline04],
        url: '/Jazz-04-DoubleBass_120.mp4',

    })



    /*
    var canvas = document.getElementById("myCanvas")
    const ctx = canvas.getContext('2d');
    ctx.beginPath(); 
    // Staring point (10,45)
    ctx.moveTo(10,45);
    // End point (180,47)
    ctx.lineTo(180,47);
    // Make the line visible
    ctx.stroke();
    */

    //var x1 = 50, y1 = 50,
    //x2 = 250, y2 = 150;
    

})


</script>

<style scoped>

</style>