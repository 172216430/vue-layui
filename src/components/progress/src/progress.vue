<template>
    <div class="layui-progress" :class="'layui-progress-' + size">
        <div class="layui-progress-bar"
             :class="'layui-bg-' + this.theme"
             :style="[
				this.color ? 'background-color: ' + this.color : '',
				{
					width: this.percentage + '%'
				}
			]">
            <span v-if="showText"
                  class="layui-progress-text">
                {{text ? text : this.percentage + '%'}}
            </span>
        </div>
    </div>
</template>
<script>
	export default {
		name: 'LayProgress',
		props: {
			percentage: Number,
			theme: String,
			color: String,
			size: String,
			showText: Boolean,
            text: String
		}
	}
</script>