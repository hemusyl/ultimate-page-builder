<template>
    <div id="upb-preview" class="upb-wrapper">
        <component v-for="(content, index) in model.contents" :key="index" :index="index" :parent="model" :model="content" :is="content._upb_options.preview.component"></component>
    </div>
</template>
<script src="./UPBPreview.js"></script>