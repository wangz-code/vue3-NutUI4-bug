<template>
	<view class="demo">
		<view> 欢迎使用 NutUI 开发 Taro 多端项目 <Dongdong /> </view>
		<view>{{ count }}</view>
		<view>
			<nut-button type="primary" @click="handleClick"> Count++ </nut-button>

			<view>
				{{ str }}
				<nut-input v-model="str" placeholder="Placeholder" />
			</view>
			<view>
				{{ num }}
				<nut-input-number v-model="num" />
			</view>
			<view>
				{{ search }}
				searchbar <nut-searchbar v-model="search"></nut-searchbar>
			</view>
		</view>
	</view>
</template>

<script setup>
import { ref } from "vue";
import { Dongdong } from "@nutui/icons-vue-taro";

const count = ref(0);
const str = ref("");
const num = ref(0);
const search = ref("");

const handleClick = () => {
	count.value++;
};
</script>

<style>
.demo {
	height: 100%;
	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;
}
</style>
