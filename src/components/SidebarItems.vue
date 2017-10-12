<template>
    <div>
        <button class="accordion" @click="show = !show">Academic</button>
        <div class="panel" v-if="show">
            <input type="checkbox" class="academic" value="Academic Clubs"/> Academic Clubs<br>
            <input type="checkbox" class="academic" value="Academic Enrichment"/> Academic Enrichment<br>
            <input type="checkbox" class="academic" value="College Credit"/> College-Credit<br>
            <input type="checkbox" class="academic" value="Credit Recovery"/> Credit Recovery<br>
            <input type="checkbox" class="academic" value="Dropout Prevention"/> Dropout Prevention<br>
            <input type="checkbox" class="academic" value="English Language Arts"/> English Language Arts<br>
            <input type="checkbox" class="academic" value="ESOL Instruction"/> ESOL Instruction<br>
            <input type="checkbox" class="academic" value="History/Social Studies"/> History/ Social Studies<br>
            <input type="checkbox" class="academic" value="Homework Help"/> Homework Help<br>
            <input type="checkbox" class="academic" value="Math"/> Math<br>
            <input type="checkbox" class="academic" value="Reading/Literature"/> Reading/ Literature<br>
            <input type="checkbox" class="academic" value="Re-Engagement"/> Re-Engagement<br>
            <input type="checkbox" class="academic" value="STEM"/> STEM<br>
            <input type="checkbox" class="academic" value="Study Skills"/> Study Skills<br>
            <input type="checkbox" class="academic" value="Test Prep: Accuplacer"/> Test Prep: Accuplacer<br>
            <input type="checkbox" class="academic" value="Test Prep: GED"/> Test Prep: GED<br>
            <input type="checkbox" class="academic" value="Test Prep: ICEE"/> Test Prep: ICEE (Exam School Test)<br>
            <input type="checkbox" class="academic" value="Test Prep: MCAS"/> Test Prep: MCAS<br>
            <input type="checkbox" class="academic" value="Test Prep: SAT"/> Test Prep: SAT<br>
            <input type="checkbox" class="academic" value="Tutoring"/> Tutoring<br>
            <input type="checkbox" class="academic" value="Unspecific Academic"/> Unspecific Academic<br>
            <button class="filterCheck" id="academicCheck"> Check All </button>
            <button class="filterUncheck" id="academicUncheck"> Uncheck All </button>
        </div>
    </div>
</template>

<script>
export default {
  data() {
      return {
          show: false
      }
  }
}
</script>

<style>
button.accordion {
    background-color: #270188;
    color: #fff;
    cursor: pointer;
    padding: 16px;
    width: 100%;
    border: none;
    text-align: left;
    outline: none;
    font-size: 15px;
    transition: 0.4s;
}

button.accordion.active, button.accordion:hover {
    background-color: #ddd;
    color: #000000;
}

button.accordion:after {
    content: '\02795';
    font-size: 13px;
    color: #777;
    float: right;
    margin-left: 5px;
}

button.accordion.active:after {
    content: "\2796";
}

div.panel {
    padding: 0;
    background-color: white;
    max-height: 900px;
    overflow: hidden;
    transition: 0.6s ease-in-out;
}
</style>
