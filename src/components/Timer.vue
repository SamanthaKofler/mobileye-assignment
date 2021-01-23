<template>
	<div class="timer flex justify-center">
            <p><span>{{convertToStr(diffDays)}}</span> days </p>
            <p><span>{{convertToStr(diffHours)}}</span> hours </p>
            <p><span>{{convertToStr(diffMins)}}</span> minutes </p>
            <p><span>{{convertToStr(diffSecs)}}</span> seconds</p>
	</div>

</template>

<script>
export default {
	data() {
		return {
			targetTime: +new Date(2021, 2, 1, 17, 0, 0),
			currTime: Date.now()
		};
	},
	computed: {
		timeDiff() {
			return this.targetTime - this.currTime;
		},
		diffDays() {
			return this.getDiffTime().days;
		},
		diffHours() {
			return this.getDiffTime().hours -  this.getDiffTime().days * 24;
		},
		diffMins() {
			return this.getDiffTime().mins - this.getDiffTime().hours * 60;
		},
		diffSecs() {
			return this.getDiffTime().secs - this.getDiffTime().mins * 60;
		},
	},
	methods: {
		updateTime(time) {
			this.currTime = time;
        },
        convertToStr(num) {
            if(num < 10) {
                return '0' + num;
            }
            else return ''+ num;
		},
		getDiffTime() {
			const days = Math.floor(this.timeDiff / (1000 * 60 * 60 * 24));
			const hours = Math.floor(this.timeDiff / (1000 * 60 * 60));
			const mins = Math.floor(this.timeDiff / (1000 * 60));
			const secs = Math.floor(this.timeDiff / 1000);
			return {days, hours, mins, secs}
		}
	},
	created() {
		setInterval(() => {
			this.updateTime(new Date());
		}, 1000);
	},
};
</script>

<style>
.timer {
	color: white;
}
</style>
