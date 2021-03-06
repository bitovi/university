@page bit-academy Bitovi Academy
@hidesidebar
@hidetitle
@hidedescription
@hidecontentnav
@description Welcome to Bitovi Academy. Learn front-end development, design,
and management in these free courses!

@body
<style>
.main-content {
  width: 100%;
  padding-right: 0;
}
.width100 {
  width: 100%;
}
.container {
  padding: 0;
}
.container .academy-section{
  border-bottom: 1px solid #e7e8e6;
  padding: 60px;
  display: flex;
  align-items: center;
  flex-direction: column;
  background-color: white;
}
.container .academy-section--grey{
  background-color: #f5f6f6;
}
.container .academy-section h3{
  font-size: 31px;
  font-weight: 300;
  margin: 0 0 30px 0;
}
.academy-section .courses-container{
  border: 2px solid red;
}
.container .academy-section .courses{
  display: flex;
  justify-content: space-between;
  align-items: stretch;
  margin-bottom: 60px;
  width: 100%;
}
.container .academy-section .courses:last-of-type{
  margin-bottom: 0;
}
.container .academy-section .courses .course{
  background-color: white;
  border: 1px solid #e7e8e6;
  padding: 30px;
  margin-right: 60px;
  flex: 1;
  text-align: left;
  min-width: 0;
  display: flex;
  justify-content: space-between;
}
.container .academy-section calendar-events.courses .course {
  justify-content: normal;
}
.container .academy-section calendar-events.courses .course .event-url {
  margin-top: auto;
}
.course h4{
  text-align: center;
}
.academy-section .courses .course a{
  text-decoration: none;
  color: #333;
}
.container .academy-section .courses .course:last-of-type{
  margin-right: 0;
}
.content {
  margin: 0;
}
.content .main{
  padding: 0;
}
.academy-card{
  border: 1px solid #e7e8e6;
  display: flex;
  flex: 1;
  flex-direction: column;
  margin-right: 60px;
  align-items: center;
  justify-content: flex-start;
  padding: 30px;
  text-align: center;
  background-color: white;
  justify-content: space-between;
}
.academy-card h4{
  font-size: 20px;
  margin: 0;
}
.academy-cards-container .academy-card:last-of-type{
  margin-right: 0;
}
.container .academy-logos{
  flex-direction: row;
  justify-content: space-between;
  padding: 30px 60px;
}
.academy-card--red{
  background-color: #ca313c;
  border-color: #ca313c;
  color: white;
  text-align: left;
  align-items: flex-end;
}
.academy-card--blue{
  background-color: #4270b7;
  border-color: #4270b7;
  color: white;
  text-align: left;
  align-items: flex-end;
}
.academy-card--orange{
  background-color: #e47c3c;
  border-color: #e47c3c;
  color: white;
  text-align: left;
  align-items: flex-end;
}
.hero-banner {
  margin-left: -30px;
  margin-right: -30px;
  background: url('./static/img/academy-banner.png') no-repeat top center;
  background-size: cover;
  background-color: #428ac9;
  text-align: center;
  padding: 60px;
}
.hero-banner h1 {
  color: #fff;
  font-family: Lato, Arial, sans-serif;
  line-height: 1.1;
  font-size: 56px;
  font-weight: 300;
  text-align: center;
  margin: 0 auto 15px auto;
}
.hero-banner h2 {
  color: #fff;
  font-size: 18px !important;
  font-weight: normal;
  line-height: 1.6;
  max-width: none;
  text-align: center;
  margin: 15px auto !important;
  margin-bottom: 30px !important;
}
.event-title{
  margin-top: 0;
}
.course .detail {
 padding: 0;
 margin: 0;
}
.details-container{
  border: 1px solid #eee;
  padding: 15px;
  margin: 0px;
  display: flex;
  flex-direction: column;
  width: 100%;
}
.button{
 padding: 5px 15px;
 background-color: #356FD1;
 border: 1px solid #356FD1;
 color: white;
 border-radius: 3px;
 text-decoration: none;
 display: inline-flex;
 align-items: center;
 justify-content: center;
}
.button:hover{
  background-color: #2F507F;
  border-color: #2F507F;
  cursor: pointer;
}
.button-large{
  padding: 10px 35px;
  font-size: 20px;
}
.button-red{
  background-color: #cb2036;
  border-color: #cb2036;
}
.button-red:hover{
  background-color: #961a2f;
  border-color: #961a2f;
}
.button-grey{
  background-color: #e5eaea;
  border-color: #d6d8d8;
  color: #333;
}
.button-grey:hover{
  background-color: #b4b5b5;
  border-color: #b4b5b5;
}
.button img{
  margin-right: 7.5px;
}
.slack-button{
  margin-top: 15px;
}
.academy-cards-container{
  display: flex;
  align-items: stretch;
  justify-content: space-between;
  flex-direction: row;
}
.academy-intro{
  padding: 60px;
}
.academy-cards-container .academy-card h4{
 margin: 0;
}
.academy-cards-container .academy-card p{
  margin: 0;
}
.academy-cards-container .academy-card:last-of-type{
  margin-right: 0px;
}
.content .main{
  padding: 0;
}
a.link{
  font-weight: 600;
  text-decoration: none;
}
.academy-card .card-image{
  margin-bottom: 30px;
}
.course-logo{
  height: 70px;
  display: flex;
  align-items: center;
  margin-bottom: 15px;
  justify-content: center;
}
p.quote-author{
  opacity: .6;
  font-size: 14px;
}
.live-events .courses{
  display: flex;
  width: 100%;
  margin-top: 30px;
  min-height: 500px;
}
.live-events .courses .academy-card{
  padding: 0;
}
.events-container{
  display: flex;
  flex: 1;
}
.academy-card .detail .event-location a{
  word-break: break-word;
  color: #356FD1;
  font-weight: 600;
}
.academy-card h4.event-title{
  margin-bottom: 17.6px;
}
.full-width{
  width: 100%;
}
.academy-card .button{
  margin-top: 30px;
}
a.quote-link{
  color: white;
  text-decoration: none;
}
a.quote-link:hover{
  opacity: .7;
}
.button-disabled{
  opacity: .3;
}
.button-disabled:hover{
  background-color: #356FD1;
  border-color: #356FD1;
  opacity: .3;
}
.academy-course-logo{
  width: 60px;
}
</style>

<div class="container">
  <div class="hero-banner">
    <h1>Level up your front-end skills</h1>
    <h2>Whether you're a beginner or a seasoned senior dev, Academy courses have something that will help you improve your JavaScript skills.</h2>
    <a class="button button-large button-red" href="#courses-section">Browse our courses</a>
  </div>
  <div class="academy-section academy-logos">
    <a href="./learn-advanced-javascript.html"><img class="academy-course-logo" src="./static/img/javascript.png"></a>
    <a href="./learn-angular.html"><img class="academy-course-logo" src="./static/img/angular.png"></a>
    <a href="./learn-dom-jquery.html"><img class="academy-course-logo" src="./static/img/jquery-logo.png"></a>
    <a href="./learn-rxjs.html"><img class="academy-course-logo" src="./static/img/rxjs.png"></a>
    <a href="./learn-typescript.html"><img class="academy-course-logo" src="./static/img/ts-logo.png"/></a>
  </div>
  <div class="academy-section page-details-section academy-section--grey">
    <div class="academy-cards-container">
      <div class="academy-card">
        <div class="academy-card--top">
          <img class="card-image" src="./static/img/academy-4.png" width="75">
          <h4>Learn by doing</h4>
          <p><a class="link" href="https://www.gse.harvard.edu/news/14/11/benefit-interactive-learning">Hands-on exercises</a> to teach you Angular, JavaScript, the DOM, TypeScript, RxJS, Angular and more.</p>
        </div>
        <a class="button full-width" href="#courses-section">Take a course</a>
      </div>
      <div class="academy-card">
        <div class="academy-card--top">
          <img class="card-image" src="./static/img/academy-2.png" width="75">
          <h4>Get help when you need it</h4>
          <p>Our team of expert front-end developers is only a slack message away.</p>
        </div>
       <a class="button slack-button full-width" href="https://www.bitovi.com/community/slack" target="\_blank"><img src="./static/img/slack-logo.svg" height="20">Join our slack community</a>
      </div>
      <div class="academy-card">
        <div class="academy-card--top">
          <img class="card-image" src="./static/img/academy-3.png" width="75">
          <h4>Leverage battle-tested trainings</h4>
          <p>The same trainings materials have been sharpened over the past decade and delivered to enterprise front-end teams at Sony, Lowes, Walmart, and more. Free and <a class="link" href="https://github.com/bitovi/academy" target="\_blank">open source</a>.</p>
        </div>
        <a class="button full-width" href="#live-events-section">See our live events</a>
      </div>
    </div>
  </div>
  <div class="academy-section">
    <h3>What people are saying about us</h3>
    <div class="academy-cards-container">
      <div class="academy-card academy-card--red">
          <p><a class="quote-link" href="https://www.meetup.com/DoneJS-Chicago/events/260347973/#commentsTitle" target="\_blank">“Really enjoyed this class! The instructor, Justin, was phenomenal, and the content was both challenging and engaging. Even though framework usage is ubiquitous these days, it's rewarding to understand exactly how libraries interact with the DOM on a granular level. I am looking forward to more Bitovi events in the future.”</a></p>
          <p class="quote-author">- Patrick Gallagher</p>
      </div>
      <div class="academy-card academy-card--blue">
        <p><a class="quote-link" href="https://www.meetup.com/DoneJS-Chicago/events/260347973/#commentsTitle" target="\_blank">“Bitovi, thanks for sharing this elite training with me. Thank you for your warmth and company, Maryann, Mike, Michael, Cherif, and Oscar, and thank you Justin for making this (another) memorable time. We went so far beyond "training" it was (as Michael would say) "sick." My best wishes of success to all.”</a></p>
        <p class="quote-author">- Carson Wilson</p>
      </div>
      <div class="academy-card academy-card--orange">
        <p><a class="quote-link" href="https://www.meetup.com/DoneJS-Chicago/events/260347973/#commentsTitle" target="\_blank">“Highly recommended! Very solid training materials which dig deep into the fundamentals of JavaScript. Justin is great at explaining complex concepts clearly and simply. I have learned a lot. Looking forward to more events!”</a></p>
        <p class="quote-author">- Shaung</p>
      </div>
    </div>
  </div>
  <a name="courses-section" class="courses-section"></a>
  <div class="academy-section academy-section--grey">
    <h3>Courses</h3>
    <div class="courses" id="courses">
      <div class="academy-card course">
          <div class="course-logo">
            <img src="./static/img/react.png" width="70">
          </div>
          <h4>React</h4>
          <p>Build a feature-rich Tic-Tac-Toe game in this beginner React guide.</p>
          <div class="width100">
            <p class='detail'><strong>Audience:</strong> Intermediate JS developers, new React developers</p>
            <p class='detail'><strong>Goal:</strong> Learn the basics of React </p>
            <p class='detail'><strong>Time:</strong> 6 hours</p>
          </div>
          <a href="./learn-react.html" class="button button-grey full-width">Take this course</a>
      </div>
      <div class="academy-card course">
          <div class="course-logo">
            <img src="./static/img/rxjs.png" height="68">
          </div>
          <h4>RxJS</h4>
          <p>Build a validating credit card form with RxJS and a bit of Angular. Learn
          the hard but fundamental operators.</p>
          <div class="width100">
            <p class='detail'><strong>Audience:</strong> Intermediate JS developers</p>
            <p class='detail'><strong>Goal:</strong> Build complex state mechanics with observables.</p>
            <p class='detail'><strong>Time:</strong> 6 hours</p>
          </div>
          <a href="./learn-rxjs.html" class="button button-grey full-width">Take this course</a>
      </div>
      <div class="academy-card course">
          <div class="course-logo">
            <img src="./static/img/angular.png" height="70">
          </div>
          <h4>Angular</h4>
          <p>Build a multipage, realtime ordering app with Angular. Learn
          FormBuilder and FormGroup. Write tests
          too!</p>
          <div class="width100">
            <p class='detail'><strong>Audience:</strong> Intermediate JS developers</p>
            <p class='detail'><strong>Goal:</strong> Build data driven applications with Angular.</p>
            <p class='detail'><strong>Time:</strong> 10 hours</p>
          </div>
          <a href="./learn-angular.html" class="button button-grey full-width">Take this course</a>
      </div>
    </div>
    <div class="courses">
      <div class="academy-card course">
          <div class="course-logo">
            <img src="./static/img/typescript.png" width="140">
          </div>
          <h4>TypeScript</h4>
          <p>Learn the essentials of TypeScript: types, functions, classes, interfaces and generics.</p>
          <div class="width100">
            <p class='detail'><strong>Audience:</strong> Beginner JS developer</p>
            <p class='detail'><strong>Goal:</strong> Be ready to develop a TypeScript project.</p>
            <p class='detail'><strong>Time:</strong> 3 hours</p>
          </div>
          <a href="./learn-typescript.html" class="button button-grey full-width">Take this course</a>
      </div>
      <div class="academy-card course">
          <div class="course-logo">
            <img src="./static/img/javascript.png" height="70">
          </div>
          <h4>Advanced JavaScript</h4>
          <p>Learn all the hard but important stuff you should know when programming JavaScript.</p>
          <div class="width100">
            <p class='detail'><strong>Audience:</strong> Intermediate JS developers</p>
            <p class='detail'><strong>Goal:</strong> Understand what's going on "under the hood".</p>
            <p class='detail'><strong>Time:</strong> 6 hours</p>
          </div>
          <a href="./learn-advanced-javascript.html" class="button button-grey full-width">Take this course</a>
      </div>
      <div class="academy-card course">
          <div class="course-logo">
            <img src="./static/img/jquery.png" width="150">
          </div>
          <h4>DOM and jQuery</h4>
          <p>Build your own version of jQuery and use it to make a basic tabs widget. Enjoy the
  meta programming too!</p>
          <div class="width100">
            <p class='detail'><strong>Audience:</strong> Intermediate JS developers</p>
            <p class='detail'><strong>Goal:</strong> Understand the DOM enough to build widgets frameworks can't.</p>
            <p class='detail'><strong>Time:</strong> 10 hours</p>
          </div>
          <a href="./learn-dom-jquery.html" class="button button-grey full-width">Take this course</a>
      </div>
    </div>
    <div class="courses">
      <div class="academy-card course">
          <div class="course-logo">
            <img src="./static/img/javascript.png" height="70">
          </div>
          <h4>Debug JavaScript</h4>
          <p>Learn breakpoints and how to debug the scope, stack, prototypes, and property changes.</p>
          <div class="width100">
            <p class='detail'><strong>Audience:</strong> Beginner JS developers</p>
            <p class='detail'><strong>Goal:</strong> Debug most problems with chrome developer tools.</p>
            <p class='detail'><strong>Time:</strong> 1 hour</p>
          </div>
          <a href="./learn-to-debug-javascript.html" class="button button-grey full-width">Take this course</a>
      </div>
      <div class="academy-card course">
          <div class="course-logo">
            <img src="./static/img/web-components.png" height="100">
          </div>
          <h4>Web Components</h4>
          <p>Build a bus tracker component that can be used anywhere with web components. Learn the core APIs.</p>
          <div class="width100">
            <p class='detail'><strong>Audience:</strong> Intermediate JS developers</p>
            <p class='detail'><strong>Goal:</strong> Understand the web component APIs at the lowest level.</p>
            <p class='detail'><strong>Time:</strong> 8 hours</p>
          </div>
          <a href="./learn-web-components.html" class="button button-grey full-width">Take this course</a>
      </div>
      <div class="academy-card course">
        <div class="course-logo">
          <img src="./static/img/docker/logo.png" height="70">
        </div>
        <h4>Docker</h4>
        <p>Build and containerize a Node app then orchestrate a more complex example with docker-compose in this Docker guide.</p>
        <div class="width100">
          <p class='detail'><strong>Audience:</strong> Intermediate developers, new DevOps Engineers</p>
            <p class='detail'><strong>Goal:</strong> Learn Docker fundamentals and container orchestration</p>
            <p class='detail'><strong>Time:</strong> 2 hours</p>
        </div>
        <a href="./learn-docker.html" class="button button-grey full-width">Take this course</a>
      </div>
    </div>
  </div>
  <a name="live-events-section"></a>
  <div class="academy-section live-events">
    <h3>Live events</h3>
    <p>Every two weeks, Bitovi hosts a live training. Subscribe to Bitovi's community calendar to be part of the next one!</p>
    <a class="button" href="https://calendar.google.com/calendar/b/1?cid=anVwaXRlcmpzLmNvbV9nMjd2Y2szNm5pZmJucXJna2N0a29hbnFiNEBncm91cC5jYWxlbmRhci5nb29nbGUuY29t"><img src="./static/img/calendar.svg" height="20"> Subscribe to our calendar</a>
  <calendar-events api-key="AIzaSyBsNpdGbkTsqn1BCSPQrjO9OaMySjK5Sns" calendar-id="jupiterjs.com_g27vck36nifbnqrgkctkoanqb4@group.calendar.google.com" event-count="3" class="courses">
    <template>
          <div class="academy-card course">
              <h4 class='event-title'></h4>
              <div class="details-container">
                <p class='detail'><strong>Date:</strong>
                  <span class='event-date'></span>
                </p>
                <p class='detail'><strong>Location:</strong>
                  <span class='event-location'></span>
                </p>
                <p class='detail'><strong>Group:</strong>
                  <span class='event-group'></span>
                </p>
              </div>
              <p class='event-body'></p>
              <a class='event-url button button-grey full-width' target="\_blank">Register for event</a>
          </div>
        </template>
      </calendar-events>
  </div>
  <div class="academy-section academy-section--grey">
    <h3>Coming soon</h3>
    <p>The following courses are under development.</p>
    <div class="courses">
      <div class="academy-card course">
          <div class="course-logo">
            <img src="./static/img/bitovi-logo-x2.png" height="70">
          </div>
          <h4>Technology Consulting</h4>
          <p>Learn to perform aspects of technology consulting:
          product management, communication, setting goals, etc.</p>
          <div class="width100">
            <p class='detail'><strong>Audience:</strong> Technology consultants or clients</p>
            <p class='detail'><strong>Goal:</strong> Learn the basics of technology consulting</p>
            <p class='detail'><strong>Time:</strong> 6 hours</p>
          </div>
          <a href="./learn-technology-consulting.html" class="button button-grey full-width">Take this course</a>
      </div>
      <div class="academy-card course">
          <div class="course-logo">
            <img src="./static/img/canjs.png" height="70">
          </div>
          <h4>CanJS</h4>
          <p>Build the TodoMVC application with CanJS 6. Learn how
             to create, update, and delete records.</p>
          <div class="width100">
            <p class='detail'><strong>Audience:</strong> Technology consultants or clients</p>
            <p class='detail'><strong>Goal:</strong> Learn the basics of CanJS </p>
            <p class='detail'><strong>Time:</strong> 6 hours</p>
          </div>
          <a href="./learn-canjs.html" class="button button-grey full-width">Take this course</a>
      </div>
      <div class="academy-card course">
        <div class="course-logo">
          <img src="./static/img/javascript.png" width="60">
        </div>
        <h4>Your Course Here</h4>
        <p>Got an idea for a course? Let us know by submitting an issue.</p>
        <a class="button full-width" style="color: white" href="https://github.com/bitovi/academy/issues/new" target="\_blank">Submit your idea</a>
      </div>
    </div>
    <div class="courses">
      <div class="academy-card course" style="background: transparent; border: none;">&nbsp;</div>
      <div class="academy-card course">
        <div class="course-logo">
          <img src="./static/img/slack.png" width="150">
        </div>
        <h4>Need Help?</h4>
        <p>Reach out to our team via Slack. We can help answer any questions you have about our courses.</p>
        <a class="button full-width" style="color: white" href="https://www.bitovi.com/community/slack" target="\_blank">Chat with us on Slack</a>
      </div>
      <div class="academy-card course" style="background: transparent; border: none;">&nbsp;</div>
    </div>
  </div>
</div>
