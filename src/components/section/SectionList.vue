<template>
    <li :class="itemClass()" @mouseover="activeFocus()" @mouseout="removeFocus()">
        <ul class="tools">
            <li v-for="(tool, id) in model._upb_options.tools.list" :key="id" @click="clickActions(id, tool)" v-if="enabled(id)" :title="tool.title" :class="toolsClass(id, tool)">
                <i :class="tool.icon"></i>
            </li>
        </ul>
        <div v-text="model.attributes.title"></div>
    </li>
</template>
<script src="./SectionList.js"></script>
