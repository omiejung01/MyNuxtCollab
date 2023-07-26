<template>
    <div class="p-10">
    <div class="align-bottom p-8 space-y-4 grid grid-cols-7 gap-4 rounded-lg border-4 max-w-5xl container mx-auto">
        <!-- <div class="rounded-lg border-4 col-span-1"> -->
        <img class="object-cover rounded-lg border-4 col-span-1 w-44" src="https://media04.tetraserver.com/uploads/videos/1667730702_Jazz-01-Piano.png"><div class="rounded-lg border-4 col-span-6 align-top h-24 "><div id="waveform01" class="border-0 w-full"></div></div>
        <img class="object-cover rounded-lg border-4 col-span-1 w-44" src="https://media04.tetraserver.com/uploads/videos/1667730837_Jazz-02-Drum.png"><div class="rounded-lg border-4 col-span-6 align-top h-24" id="waveform02"></div>
        <img class="object-cover rounded-lg border-4 col-span-1 w-44" src="https://media04.tetraserver.com/uploads/videos/1667731195_Jazz-03-Saxophone.png"><div class="rounded-lg border-4 col-span-6 align-top h-24" id="waveform03"></div>
        <img class="object-cover rounded-lg border-4 col-span-1 w-44" src="https://media04.tetraserver.com/uploads/videos/1667731377_Jazz-04-DoubleBass.png"><div class="rounded-lg border-4 col-span-6 align-top h-24" id="waveform04"></div>
        
    </div>
</div>
</template>

<script setup>

onMounted(() => {
    var waveform = document.getElementById("waveform01");

    var wavesurfer = WaveSurfer.create({
        container: '#waveform01',
        waveColor: 'violet',
        maxCanvasWidth: 600,
        height:96,
        mediaContainer: waveform,
        progressColor: 'purple'
    });

    wavesurfer.load('/Jazz-01-Piano_120.mp4');
    

})
</script>

<style scoped>

</style>