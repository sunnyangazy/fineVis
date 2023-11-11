<!-- <template>
  <div class="app">
    <div class="column">
      <div class="sub-column"></div>
      <div class="sub-column"></div>
      <div class="sub-column"></div>
      <div class="sub-column"></div>
      <div class="sub-column"></div>
    </div>
    <div class="column">
      <h1>Column 2</h1>
    </div>
    <div class="column">
      <h1>Column 3</h1>
    </div>
  </div>
</template>

<style>
.app {
  display: flex;
}

.column {
  flex: 1;
  height: 100vh; /* 可根据需要调整高度 */
  border: 1px solid #000; /* 可自定义边框样式 */
}

.sub-column {
  flex: 1;
  height: 19vh; /* 可根据需要调整高度 */
  border: 1px solid #000; /* 可自定义边框样式 */
  margin-bottom: 5px; /* 添加间距，可根据需要调整 */
}
</style> -->

<template>
  <div class="app">
    <div class="column">
      <div class="sub-column" ref="lineChart1"></div>
      <div class="sub-column" ref="lineChart2"></div>
      <div class="sub-column" ref="lineChart3"></div>
      <div class="sub-column" ref="lineChart4"></div>
      <div class="sub-column" ref="barChart"></div>
    </div>
    <div class="column">
      <h1>Column 2</h1>
    </div>
    <div class="column">
      <h1>Column 3</h1>
    </div>
  </div>
</template>

<script>
import * as echarts from 'echarts';

export default {
  mounted() {
    this.drawCharts();
  },
  methods: {
    drawCharts() {
      // 绘制折线图1
      const lineChart1 = echarts.init(this.$refs.lineChart1);

      const lineData1 = [
        { month: 'Jan', value: 30 },
        { month: 'Feb', value: 40 },
        { month: 'Mar', value: 20 },
        { month: 'Apr', value: 50 },
        { month: 'May', value: 10 }
      ];

      const lineOption1 = {
        xAxis: {
          type: 'category',
          data: lineData1.map((d) => d.month)
        },
        yAxis: {
          type: 'value'
        },
        series: [
          {
            type: 'line',
            data: lineData1.map((d) => d.value)
          }
        ]
      };

      lineChart1.setOption(lineOption1);

      // 绘制折线图2
      const lineChart2 = echarts.init(this.$refs.lineChart2);

      const lineData2 = [
        { month: 'Jan', value: 50 },
        { month: 'Feb', value: 20 },
        { month: 'Mar', value: 30 },
        { month: 'Apr', value: 40 },
        { month: 'May', value: 25 }
      ];

      const lineOption2 = {
        xAxis: {
          type: 'category',
          data: lineData2.map((d) => d.month)
        },
        yAxis: {
          type: 'value'
        },
        series: [
          {
            type: 'line',
            data: lineData2.map((d) => d.value)
          }
        ]
      };

      lineChart2.setOption(lineOption2);

      // 绘制折线图3
      const lineChart3 = echarts.init(this.$refs.lineChart3);

      const lineData3 = [
        { month: 'Jan', value: 15 },
        { month: 'Feb', value: 35 },
        { month: 'Mar', value: 45 },
        { month: 'Apr', value: 10 },
        { month: 'May', value: 30 }
      ];

      const lineOption3 = {
        xAxis: {
          type: 'category',
          data: lineData3.map((d) => d.month)
        },
        yAxis: {
          type: 'value'
        },
        series: [
          {
            type: 'line',
            data: lineData3.map((d) => d.value)
          }
        ]
      };

      lineChart3.setOption(lineOption3);

      // 绘制折线图4
      const lineChart4 = echarts.init(this.$refs.lineChart4);

      const lineData4 = [
        { month: 'Jan', value: 40 },
        { month: 'Feb', value: 20 },
        { month: 'Mar', value: 10 },
        { month: 'Apr', value: 30 },
        { month: 'May', value: 5 }
      ];

      const lineOption4 = {
        xAxis: {
          type: 'category',
          data: lineData4.map((d) => d.month)
        },
        yAxis: {
          type: 'value'
        },
        series: [
          {
            type: 'line',
            data: lineData4.map((d) => d.value)
          }
        ]
      };

      lineChart4.setOption(lineOption4);

      // 绘制条形图
      const barChart = echarts.init(this.$refs.barChart);

      const barData = [
        { label: 'A', value: 10 },
        { label: 'B', value: 20 },
        { label: 'C', value: 15 },
        { label: 'D', value: 25 },
        { label: 'E', value: 5 }
      ];

      const barOption = {
        xAxis: {
          type: 'category',
          data: barData.map((d) => d.label)
        },
        yAxis: {
          type: 'value'
        },
        series: [
          {
            type: 'bar',
            data: barData.map((d) => d.value)
          }
        ]
      };

      barChart.setOption(barOption);
    }
  }
};
</script>

<style>
.app {
  display: flex;
}

.column {
  flex: 1;
  height: 100vh;
  border: 1px solid #000;
}

.sub-column {
  flex: 1;
  height: 22vh;
  border: 1px solid #000;
  margin-bottom: 5px;
}
</style>