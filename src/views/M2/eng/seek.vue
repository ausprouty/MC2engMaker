<script>
import {useShare} from "@/assets/javascript/share.js"

export default {

  methods:{
    vuePush(id){
      this.$router.push({
        name: id,
      })
    },
    share(what, v1, v2){
      useShare(what, v1, v2)
    }
  },
  mounted() {
    localStorage.setItem("returnpage", this.$route.name)
  }
}
</script>
<template>
  <!-- sdcard template from mc2 -->

  <div class="page_content" dir="ltr">
    <div id="nav">
      <div class="nav full internal-link" @click="this.vuePush('eng-index')">
          <img src="@/assets/sites/mc2/images/ribbons/back-ribbon-mc2.png" class="nav full" />
      </div>
  </div>
    <div>
      <!-- begin mc2 sdcard bookImage -->
<div class="Xapp-link">
  <div class="card-link" @click="vuePush('eng-hope-index')">
    <div class="Xapp-card -Xshadow">
      <img src="@/assets/sites/mc2/content/M2/images/standard/Stories-of-Hope.png" class="book-large" />
    </div>
  </div>
</div>
<!-- end mc2 sdcard bookImage -->
<!-- begin mc2 sdcard bookImage -->
<div class="Xapp-link">
  <div class="card-link" @click="vuePush('eng-prophet-index')">
    <div class="Xapp-card -Xshadow">
      <img src="@/assets/sites/mc2/content/M2/images/standard/Stories-of-the-Prophets.png" class="book-large" />
    </div>
  </div>
</div>
<!-- end mc2 sdcard bookImage -->

    </div>
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

			<td class="social" @click="share('lesson', 'seek: ', '/content/M2/eng/seek.html')">
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
</div>
<!-- end default library -->
</template>
<!--- Created by publishLibrary-->
<!-- begin sdcard Footer -->
<!-- end sdcard Footer -->