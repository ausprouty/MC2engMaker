<script>
import SQLiteService from '@/services/SQLiteService.js'
import { useFindSummaries, useFindCollapsible, usePopUp} from "@/assets/javascript/revealText.js"
import { useRevealMedia } from "@/assets/javascript/revealMedia.js"
import { useShare} from "@/assets/javascript/share.js"


export default {
   methods:{
    async addNote(noteid){
       var noteText = document.getElementById(noteid).value
       var noteHeight = await SQLiteService.addNote(noteid, this.$route.name, noteText)
       document.getElementById(noteid).style.height = noteHeight
    },
    goToPageAndSetReturn(gotoPath){
      localStorage.setItem("returnpage", this.$route.name);
      this.$router.push({
        path: gotoPath,
      })
    },
    pageGoBack(returnto){
      if (localStorage.getItem("returnpage")) {
        returnto = localStorage.getItem("returnpage");
        localStorage.removeItem("returnpage")
      }
      this.$router.push({
        name: returnto,
      })
    },
    popUp(verse){
      usePopUp(verse)
    },
    share(what, v1, v2){
      useShare(what, v1, v2)
    },
    vuePush(id){
      this.$router.push({
        name: id,
      })
    },
  },
  async mounted() {
    localStorage.setItem("lastpage", this.$route.name)
    useFindSummaries()
    useFindCollapsible()
    useRevealMedia()
    await SQLiteService.notes(this.$route.name)
  },
}
</script>
<template>
  <div id="nav">
    <div class="nav full internal-link" @click="this.pageGoBack('eng-hope-index')">
        <img src="@/assets/sites/mc2/images/ribbons/mc2back.png" class="nav full" />
    </div>
</div>
<div class="page_content ltr">
<div class="block ltr">
                        <div class="chapter_number ltr"><h1>2.</h1></div>
                        <div class="chapter_title ltr"><h1>Hope for the Non-Religious</h1></div>
                    </div>
<div id="showVideoOptions"></div>
  <div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-back.png" />
<div class="lesson-subtitle"><span class="back">LOOK BACK</span></div>
</div>

<div>
<h2>Caring for one another</h2>

<ul>
	<li>What has been a highlight this week?</li>
	<li>What has been a challenge this week?</li>
	<li>What do you want Jesus to do for you this week?</li>
	<li>Briefly pray for&nbsp; Jesus to meet the needs that are shared.</li>
</ul>

<h2>Celebrate Faithfulness</h2>

<ul>
	<li>How did you obey Jesus last week?</li>
	<li>Who did you share the story with last week?</li>
</ul>

<h2>Motivation and Encouragement</h2>

<ul>
	<li>Encourage each other to keep obeying Jesus and remind each other of the importance of sharing the stories with others.</li>
</ul>
</div>

<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-up.png" />
<div class="lesson-subtitle"><span class="up">LOOK UP</span></div>
</div>

<h2>Discover the Bible together</h2>

<!-- begin default revealSummary -->
<div id="Summary0" class="summary"><h2>+ Context</h2></div>
<div class="collapsed" id ="Text0">
<!-- end default revealSummary -->

<p>We learned about Pharisees in the first story of hope. They were the religious leaders. They were very careful to avoid non-religious people. The tax collectors were not respected by Pharisees. They were often corrupt and took bribes from people rather than collecting the proper tax. Jesus told a story of a Pharisee and a tax collector who were worshipping God. They prayed to God very differently.</p>

</div>

<h2>Read</h2>

<ul>
	<li>
	<p>Read or watch Luke 18:9-17 two times as others listen.</p>
	</li>
</ul>

<button id="Button0" type="button" class="collapsible bible">Read Luke 18:9-17</button><div class="collapsed" id ="Text0">
<!-- begin bible -->

<h3>The Parable of the Pharisee and the Tax Collector</h3>

<p><sup class="versenum">9&nbsp;</sup>To some who were confident of their own righteousness and looked down on everyone else, Jesus told this parable:<sup class="versenum">10&nbsp;</sup>&ldquo;Two men went up to the temple to pray, one a Pharisee and the other a tax collector.<sup class="versenum">11&nbsp;</sup>The Pharisee stood by himself and prayed: &lsquo;God, I thank you that I am not like other people&mdash;robbers, evildoers, adulterers&mdash;or even like this tax collector.<sup class="versenum">12&nbsp;</sup>I fast twice a week and give a tenth of all I get.&rsquo;</p>

<p><sup class="versenum">13&nbsp;</sup>&ldquo;But the tax collector stood at a distance. He would not even look up to heaven, but beat his breast and said, &lsquo;God, have mercy on me, a sinner.&rsquo;</p>

<p><sup class="versenum">14&nbsp;</sup>&ldquo;I tell you that this man, rather than the other, went home justified before God. For all those who exalt themselves will be humbled, and those who humble themselves will be exalted.&rdquo;</p>

<h3>The Little Children and Jesus</h3>

<p><sup class="versenum">15&nbsp;</sup>People were also bringing babies to Jesus for him to place his hands on them. When the disciples saw this, they rebuked them.<sup class="versenum">16&nbsp;</sup>But Jesus called the children to him and said, &ldquo;Let the little children come to me, and do not hinder them, for the kingdom of God belongs to such as these.<sup class="versenum">17&nbsp;</sup>Truly I tell you, anyone who will not receive the kingdom of God like a little child will never enter it.&rdquo;</p>
<!-- end bible -->

<p class="bible"></p>

</div>

<button id="MC2/eng/video/hope/02.mp4" type="button" class="external-movie">
         Watch &nbsp;Luke 18:9-17&nbsp;</button>
    <div class="collapsed"></div>

<h2>Discovery Discussion</h2>

<ul>
	<li>What caught your attention in this story and why?</li>
	<li>What do we learn about Jesus?</li>
	<li>What do we learn about people?</li>
	<li>Who do you most identify with in the story the most and why?</li>
	<li>What keeps you from following Jesus today?</li>
</ul>

<h2>Read, Tell and Correct</h2>

<ul>
	<li>Read the story again. Ask someone to tell the story from memory. The group can help if necessary.</li>
</ul>

<!-- begin default revealSummary -->
<div id="Summary1" class="summary"><h2>+ Summary</h2></div>
<div class="collapsed" id ="Text1">
<!-- end default revealSummary -->

<p>The Pharisee was condemned by Jesus because his attitude was not humble and repentant. The tax collector was approved by Jesus because of his humble attitude. Jesus says that even a non-religious person like the tax collector can be justified before God through a humble attitude. We must recognize that we are sinful people and humble ourselves before God like the tax collector.</p>

</div>

<p>&nbsp;</p>

<!-- begin note capacitor-->
<div class="note-area">
    <form class="auto_submit_item">
      <textarea
        class="textarea resize-ta"
        @keyup="this.addNote('note1Text')"
        id="note1Text"
      ></textarea>
    </form>
</div>
<!-- end note capacitor -->


<div class="lesson"><img class="lesson-icon" src="@/assets/sites/mc2/images/standard/look-forward.png" />
<div class="lesson-subtitle"><span class="forward">LOOK FORWARD</span></div>
</div>

<h2>Practice</h2>

<ul>
	<li>Pair up and practice telling the story together</li>
</ul>

<h2>Choose something to obey together</h2>

<ul>
	<li>How can we follow this teaching?</li>
	<li>Is there anyone we can serve in simple ways this week?</li>
	<li>Who is someone in your life that you think needs to hear this story?</li>
</ul>

<!-- begin note capacitor-->
<div class="note-area">
    <form class="auto_submit_item">
      <textarea
        class="textarea resize-ta"
        @keyup="this.addNote('note2Text')"
        id="note2Text"
      ></textarea>
    </form>
</div>
<!-- end note capacitor -->


<h2>Pray</h2>

<ul>
	<li>Thank God for the time together and ask God to help each one to know HIm better.</li>
</ul>


<!-- begin mc2 sdcard languageFooter -->

<div class="languages" id="languages"><img class="languages" src="@/assets/sites/mc2/images/standard/OtherLanguagesTop.png" /></div>
<table class="social">
	<tbody>
		<tr>
			<td class="social" @click="share('languages', '', '')">
				  <img class="social" src="@/assets/sites/mc2/images/menu/languages.png" />
			  </td>
			  
			<td class="social"  @click="share('android', 'eng', '')">
				<img  class="social" src="@/assets/sites/mc2/images/standard/android.png" />
			</td>

			<td class="social" @click="share('lesson', 'Hope for the Non-Religious: ', '/content/M2/eng/hope/hope02.html')">
				<img class="social" src="@/assets/sites/mc2/images/standard/Share.png" />
			</td>
		</tr>
	</tbody>
</table>
<div class="footer">
<p class="footer">MC2</p>
<p class="footer" @click="share('website', 'https://GlobalChurchMovements.org', '')"> GlobalChurchMovements.org</p>
</div>

<!-- end mc2 sdcard languageFooter -->
</div><!--- Created by publishPage-->

</template>
<!-- begin sdcard Footer -->
<!-- end sdcard Footer -->