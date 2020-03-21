<template>
  <div id="app">
    <div class="nav-bar">
      <router-link to="/">Home</router-link> 
      <router-link to="/about">About</router-link> 
      <router-link to="/professor">Professor</router-link>
    </div>
    <router-view />
  </div>
</template>



<style>
body {
   font-family: tahoma;
   color:#282828;
   margin: 0px;
 }

 .product {
   display: flex;
   flex-flow: wrap;
   padding: 1rem;
 }

 img {
   border: 1px solid #d8d8d8;
   width: 70%;
   margin: 40px;
   box-shadow: 0px .5px 1px #d8d8d8;
 }

 .product-image {
   width: 80%;
 }

 .product-image,
 .product-info {
   margin-top: 10px;
   width: 50%;
 }

 .color-box {
   width: 40px;
   height: 40px;
   margin-top: 5px;
 }

 .cart {
   float: right;
   margin-right: 25px;
   border: 1px solid #d8d8d8;
   padding: 5px 20px;
   width: 10%;
   margin-top: 100px;
   background: linear-gradient(-90deg, #84CF6A, #16C0B0);
   color: white;
 }

 button {
   margin-top: 30px;
   margin-right: 10px;
   border: none;
   background-color: #1E95EA;
   color: white;
   height: 40px;
   width: 100px;
   font-size: 14px;
 }

.add {
   float: left;
 }
 .remove {
   float: left;
 }

 .disabledButton {
   background-color: #d8d8d8;
 }

 .review-form {
   width: 400px;
   padding: 20px;
   margin: 40px;
   border: 1px solid #d8d8d8;
 }

 input {
   width: 100%;
   height: 25px;
   margin-bottom: 20px;
 }

 textarea {
   width: 100%;
   height: 60px;
 }

 .tab {
   margin-left: 20px;
   cursor: pointer;
 }

 .activeTab {
   color: #16C0B0;
   text-decoration: underline;
 }

 .names {
   font-size: 20px;
   margin: 20px;
   text-align: center;
 }

 .names p:hover {
   color: #1E95EA;
 }

.nav-bar {
   background: linear-gradient(-90deg, #84CF6A, #16C0B0);
   height: 60px;
 }
 .nav-bar > a {
   padding-top: 20px;
   display: inline-block;
   margin: 10px;
   text-decoration: none;
 }
 .footer {
  text-align: center;
  background: linear-gradient(-90deg, #84CF6A, #16C0B0);
  height: 60px;
}
</style>
