<template>
  <div class="about">
    <div class="about-header">
     <h1>Why use this site instead of others?</h1>
    </div>

    <div class="about-image">
      <img src="images/mountain.jpg" alt="mountain">
    </div>

      <div class="about-content">
        <div class="about-para">
          <p>You should use this site to choose your classes because it's better than other sites, straight up!</p>
          <p>Here is a couple of the reasons you might want to know</p>
        </div>
        <div class="about-list">
          <ul>
            <li class="list">I Benjamin Harden made this website!</li>
            <li class="list">This website uses vue. Which is cool, kinda painful, but cool</li>
            <li class="list">When you add classes and then switch pages, the website will reset all your classes to zero</li>
            <li class="list">Some may think this is a bug, but it's not, it's a feature!! I meant it to be that way, because at a time like this nobody should be in school</li>
            <li class="list">Some may think this is a bug, but it's not, it's a feature!! I meant it to be that way, because at a time like this nobody should be in school</li>
            <li class="list"> If I had wanted to I would have put my data in the App.vue file and accessed them differnetly to make it so your classes stayed, but, That's not what I wanted</li>
          </ul>
        </div>
      </div>
      <div class="footer">
        <p>Thank you for grading kindly<br>github repo: <a href="https://github.com/bharden/vue-creative-project-fun.git">https://github.com/bharden/vue-creative-project-fun.git</a></p>
      </div>
    </div>
</template>

<style scoped>
.about-header {
  text-align: center;
}
.about-image {
  float: left;
  width: 50%;
}
.about-content{
  float: right;
  width: 50%;
  margin-top: 50px;
  font-size: 30px;
}
.about-para {
  text-align: center;
}

.list {
  padding: 5px;
  margin: 10px;
}
.footer {
  clear: both;
}

</style>
