<template>
    <div class="editor">
        <div ref="editorContainer" class="container"></div>
    </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import { editor } from 'monaco-editor';

@Component({
    components: {},
})
export default class Editor extends Vue {
    private mounted() {
        editor.create(this.$refs.editorContainer as HTMLElement);
    }
}
</script>

<style lang="less" scoped>
.editor {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.container {
    display: block;
    width: 960px;
    height: 600px;
}
</style>