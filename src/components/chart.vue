<template>
  <div>
    <organization-chart :datasource="ds"></organization-chart>
  </div>
</template>

<script>
import vue from "vue";
import OrganizationChart from "vue-organization-chart";
import "vue-organization-chart/dist/orgchart.css";

export default {
  components: {
    OrganizationChart
  },
  data() {
    return {
      ds: {
        name: "해지",
        title: "46.1%➥44.1% ⇧ 36,765",
        children: [
          { name: "14일이내 멜론재구매", title: "46.1%➥44.1% ⇧ 36,765" },
          {
            name: "14일이내 멜론미구매",
            title: "46.1%➥44.1% ⇧ 36,765",
            children: [
              {
                name: "멜론 미이용",
                title: "46.1%➥44.1% ⇧ 36,765",
                children: [
                  { name: "멜론 재구매", title: "46.1%➥44.1% ⇧ 36,765" }
                ]
              },
              {
                name: "Churn-out",
                title: "46.1%➥44.1% ⇧ 36,765",
                children: [
                  {
                    name: "Churn-in",
                    title: "46.1%➥44.1% ⇧ 36,765",
                    children: [
                      { name: "지니뮤직", title: "46.1%➥44.1% ⇧ 36,765" },
                      { name: "지니뮤직", title: "46.1%➥44.1% ⇧ 36,765" },
                      { name: "지니뮤직", title: "46.1%➥44.1% ⇧ 36,765" },
                      { name: "지니뮤직", title: "46.1%➥44.1% ⇧ 36,765" },
                      { name: "지니뮤직", title: "46.1%➥44.1% ⇧ 36,765" },
                      { name: "지니뮤직", title: "46.1%➥44.1% ⇧ 36,765" },
                      { name: "지니뮤직", title: "46.1%➥44.1% ⇧ 36,765" },
                      { name: "지니뮤직", title: "46.1%➥44.1% ⇧ 36,765" }
                    ]
                  },
                  { name: "지니뮤직", title: "46.1%➥44.1% ⇧ 36,765" },
                  { name: "지니뮤직", title: "46.1%➥44.1% ⇧ 36,765" },
                  { name: "지니뮤직", title: "46.1%➥44.1% ⇧ 36,765" },
                  { name: "지니뮤직", title: "46.1%➥44.1% ⇧ 36,765" },
                  { name: "지니뮤직", title: "46.1%➥44.1% ⇧ 36,765" },
                  { name: "지니뮤직", title: "46.1%➥44.1% ⇧ 36,765" }
                ]
              }
              // { 'name': 'Churn-in', 'title': '46.1%➥44.1% ⇧ 36,765' ,
              // 'children': [
              //   { 'name': '지니뮤직', 'title': '46.1%➥44.1% ⇧ 36,765'  },
              //   { 'name': '지니뮤직', 'title': '46.1%➥44.1% ⇧ 36,765'  },
              //   { 'name': '지니뮤직', 'title': '46.1%➥44.1% ⇧ 36,765'  },
              //   { 'name': '지니뮤직', 'title': '46.1%➥44.1% ⇧ 36,765'  },
              //   { 'name': '지니뮤직', 'title': '46.1%➥44.1% ⇧ 36,765'  },
              //   { 'name': '지니뮤직', 'title': '46.1%➥44.1% ⇧ 36,765'  },
              //   { 'name': '지니뮤직', 'title': '46.1%➥44.1% ⇧ 36,765'  },
              //   { 'name': '지니뮤직', 'title': '46.1%➥44.1% ⇧ 36,765'  }
              // ]}
            ]
          }
        ]
      }
    };
  }
};
</script>
<style>
.orgchart {
  box-sizing: border-box;
  display: inline-block;
  min-height: 202px;
  min-width: 202px;
  -webkit-touch-callout: none;
  -webkit-user-select: none;
  -khtml-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
  background-size: 10px 10px;
  background-color: #fff;
  border: 1px dashed transparent;
  padding: 20px;
}
.orgchart .hidden,
.orgchart ~ .hidden {
  display: none;
}
.orgchart.b2t {
  transform: rotate(180deg);
}
.orgchart {
  position: absolute;
  left: 0;
  transform: rotate(-90deg) rotateY(180deg);
  transform-origin: left top;
}
.orgchart .verticalNodes ul {
  list-style: none;
  margin: 0;
  padding-left: 18px;
  text-align: left;
}
.orgchart .verticalNodes ul:first-child {
  margin-top: 2px;
}
.orgchart .verticalNodes > td::before {
  content: "";
  border: 1px solid rgba(217, 83, 79, 0.8);
}
.orgchart .verticalNodes > td > ul > li:first-child::before {
  box-sizing: border-box;
  top: -4px;
  height: 30px;
  width: calc(50% - 2px);
  border-width: 2px 0 0 2px;
}
.orgchart .verticalNodes ul > li {
  position: relative;
}
.orgchart .verticalNodes ul > li::after,
.orgchart .verticalNodes ul > li::before {
  box-sizing: border-box;
  content: "";
  position: absolute;
  left: -6px;
  border-color: rgba(217, 83, 79, 0.8);
  border-style: solid;
  border-width: 0 0 2px 2px;
}
.orgchart .verticalNodes ul > li::before {
  top: -4px;
  height: 30px;
  width: 11px;
}
.orgchart .verticalNodes ul > li::after {
  top: 1px;
  height: 100%;
}
.orgchart .verticalNodes ul > li:first-child::after {
  box-sizing: border-box;
  top: 24px;
  width: 11px;
  border-width: 2px 0 0 2px;
}
.orgchart .verticalNodes ul > li:last-child::after {
  box-sizing: border-box;
  border-width: 2px 0 0;
}
.orgchart.r2l {
  position: absolute;
  transform: rotate(90deg);
  transform-origin: left top;
}
.orgchart > .spinner {
  font-size: 100px;
  margin-top: 30px;
  color: rgba(68, 157, 68, 0.8);
}
.orgchart table {
  border-spacing: 0;
  border-collapse: separate;
}
.orgchart > table:first-child {
  margin: 20px auto;
}
.orgchart td {
  text-align: center;
  vertical-align: top;
  padding: 0;
}
.orgchart .lines:nth-child(3) td {
  box-sizing: border-box;
  height: 20px;
}
.orgchart .lines .topLine {
  border-top: 2px solid rgba(217, 83, 79, 0.8);
}
.orgchart .lines .rightLine {
  border-right: 1px solid rgba(217, 83, 79, 0.8);
  float: none;
  border-radius: 0;
}
.orgchart .lines .leftLine {
  border-left: 1px solid rgba(217, 83, 79, 0.8);
  float: none;
  border-radius: 0;
}
.orgchart .lines .downLine {
  background-color: rgba(217, 83, 79, 0.8);
  margin: 0 auto;
  height: 20px;
  width: 2px;
  float: none;
}
.orgchart .node {
  box-sizing: border-box;
  display: inline-block;
  position: relative;
  margin: 0;
  padding: 3px;
  border: 2px dashed transparent;
  text-align: center;
  width: 130px;
}
.orgchart .node,
.orgchart.r2l .node {
  width: 50px;
  height: 130px;
}
.orgchart .node > .spinner {
  position: absolute;
  top: calc(50% - 15px);
  left: calc(50% - 15px);
  vertical-align: middle;
  font-size: 30px;
  color: rgba(68, 157, 68, 0.8);
}
.orgchart .node:hover {
  background-color: rgba(238, 217, 54, 0.5);
  transition: 0.5s;
  cursor: default;
  z-index: 20;
}
.orgchart .node.focused {
  background-color: rgba(238, 217, 54, 0.5);
}
.orgchart .ghost-node {
  position: fixed;
  left: -10000px;
  top: -10000px;
}
.orgchart .ghost-node rect {
  fill: #fff;
  stroke: #bf0000;
}
.orgchart .node.allowedDrop {
  border-color: rgba(68, 157, 68, 0.9);
}
.orgchart .node .title {
  text-align: center;
  font-size: 12px;
  font-weight: 700;
  height: 20px;
  line-height: 20px;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
  background-color: rgba(217, 83, 79, 0.8);
  color: #fff;
  border-radius: 4px 4px 0 0;
}
.orgchart.b2t .node .title {
  transform: rotate(-180deg);
  transform-origin: center bottom;
}
.orgchart .node .title {
  transform: rotate(-90deg) translate(-40px, -40px) rotateY(180deg);
  transform-origin: bottom center;
  width: 120px;
}
.orgchart.r2l .node .title {
  transform: rotate(-90deg) translate(-40px, -40px);
  transform-origin: bottom center;
  width: 120px;
}
.orgchart .node .title .symbol {
  float: left;
  margin-top: 4px;
  margin-left: 2px;
}
.orgchart .node .content {
  box-sizing: border-box;
  width: 100%;
  height: 20px;
  font-size: 11px;
  line-height: 18px;
  border: 1px solid rgba(217, 83, 79, 0.8);
  border-radius: 0 0 4px 4px;
  text-align: center;
  background-color: #fff;
  color: #333;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.orgchart.b2t .node .content {
  transform: rotate(180deg);
  transform-origin: center top;
}
.orgchart .node .content {
  transform: rotate(-90deg) translate(-40px, -40px) rotateY(180deg);
  transform-origin: top center;
  width: 120px;
}
.orgchart.r2l .node .content {
  transform: rotate(-90deg) translate(-40px, -40px);
  transform-origin: top center;
  width: 120px;
}
.orgchart .node .edge {
  font-size: 15px;
  position: absolute;
  color: rgba(68, 157, 68, 0.5);
  cursor: default;
  transition: 0.2s;
}
.orgchart.noncollapsable .node .edge {
  display: none;
}
.orgchart .edge:hover {
  color: #449d44;
  cursor: pointer;
}
.orgchart .node .verticalEdge {
  width: calc(100% - 10px);
  width: -webkit-calc(100% - 10px);
  width: -moz-calc(100% - 10px);
  left: 5px;
}
.orgchart .node .topEdge {
  top: -4px;
}
.orgchart .node .bottomEdge {
  bottom: -4px;
}
.orgchart .node .horizontalEdge {
  width: 15px;
  height: calc(100% - 10px);
  height: -webkit-calc(100% - 10px);
  height: -moz-calc(100% - 10px);
  top: 5px;
}
.orgchart .node .rightEdge {
  right: -4px;
}
.orgchart .node .leftEdge {
  left: -4px;
}
.orgchart .node .horizontalEdge::before {
  position: absolute;
  top: calc(50% - 7px);
}
.orgchart .node .rightEdge::before {
  right: 3px;
}
.orgchart .node .leftEdge::before {
  left: 3px;
}
.orgchart .node .toggleBtn {
  position: absolute;
  left: 5px;
  bottom: -2px;
  color: rgba(68, 157, 68, 0.6);
}
.orgchart .node .toggleBtn:hover {
  color: rgba(68, 157, 68, 0.8);
}
.oc-export-btn {
  display: inline-block;
  position: absolute;
  right: 5px;
  top: 5px;
  padding: 6px 12px;
  margin-bottom: 0;
  font-size: 14px;
  font-weight: 400;
  line-height: 1.42857143;
  text-align: center;
  white-space: nowrap;
  vertical-align: middle;
  touch-action: manipulation;
  cursor: pointer;
  user-select: none;
  color: #fff;
  background-color: #5cb85c;
  border: 1px solid transparent;
  border-color: #4cae4c;
  border-radius: 4px;
}
.oc-export-btn[disabled] {
  cursor: not-allowed;
  box-shadow: none;
  opacity: 0.3;
}
.oc-export-btn:active,
.oc-export-btn:focus,
.oc-export-btn:hover {
  background-color: #449d44;
  border-color: #347a34;
}
.orgchart ~ .mask {
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 999;
  text-align: center;
  background-color: rgba(0, 0, 0, 0.3);
}
.orgchart ~ .mask .spinner {
  position: absolute;
  top: calc(50% - 54px);
  left: calc(50% - 54px);
  color: rgba(255, 255, 255, 0.8);
  font-size: 108px;
}
.orgchart .node {
  transition: transform 0.3s, opacity 0.3s;
}
.orgchart .slide-down {
  opacity: 0;
  transform: translateY(40px);
}
.orgchart .node.slide-down,
.orgchart.r2l .node.slide-down {
  transform: translateY(130px);
}
.orgchart .slide-up {
  opacity: 0;
  transform: translateY(-40px);
}
.orgchart .node.slide-up,
.orgchart.r2l .node.slide-up {
  transform: translateY(-130px);
}
.orgchart .slide-right {
  opacity: 0;
  transform: translateX(130px);
}
.orgchart .node.slide-right,
.orgchart.r2l .node.slide-right {
  transform: translateX(40px);
}
.orgchart .slide-left {
  opacity: 0;
  transform: translateX(-130px);
}
.orgchart .node.slide-left,
.orgchart.r2l .node.slide-left {
  transform: translateX(-40px);
}
.orgchart {
  background: white;
}
.orgchart .node {
  height: 200px;
}
.orgchart .node .title {
  background-color: transparent;
  color: #333;
  font-size: 14px;
}
.orgchart .node .content {
  width: 200px;
  border: 0 none;
  background-color: transparent;
  font-size: 14px;
  margin: 42px -37px 0px;
  text-align: left;
}
.orgchart .lines .topLine,
.orgchart .lines .leftLine,
.orgchart .lines .rightLine {
  border-color: #333;
}
.orgchart .lines .downLine {
  background-color: #333;
}
.nodes .nodes td:nth-child(2) > table:first-child {
  position: relative;
  top: 0;
  left: 150px;
}
.nodes
  .nodes
  td:nth-child(2)
  tr:first-child
  table:first-child
  tr:first-child
  td {
  /* position:relative;
  width:50px;
  height:200px; */
}
</style>