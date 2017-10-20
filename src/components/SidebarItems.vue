<template>
    <div>
        <button class="accordion" @click="showAcademic = !showAcademic">Academic</button>
        <div class="panel" v-if="showAcademic">
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

        <button class="accordion" @click="showArts = !showArts">Arts and Culture</button>
        <div class="panel" v-if="showArts">
            <input type="checkbox" class="ArtsAndCulture" value="Architecture/ Planning"/> Architecture/ Planning<br>
            <input type="checkbox" class="ArtsAndCulture" value="Choreography"/> Choreography<br>
            <input type="checkbox" class="ArtsAndCulture" value="Comedy/Improvisation"/> Comedy/Improvisation<br>
            <input type="checkbox" class="ArtsAndCulture" value="Craft/folk Art"/> Craft/folk Art<br>
            <input type="checkbox" class="ArtsAndCulture" value="Creative Writing"/> Creative Writing<br>
            <input type="checkbox" class="ArtsAndCulture" value="Culinary Education"/> Culinary Education<br>
            <input type="checkbox" class="ArtsAndCulture" value="Dance"/> Dance<br>
            <input type="checkbox" class="ArtsAndCulture" value="Drawing"/> Drawing<br>
            <input type="checkbox" class="ArtsAndCulture" value="Fashion"/> Fashion<br>
            <input type="checkbox" class="ArtsAndCulture" value="Film/Video Production"/> Film/Video Production<br>
            <input type="checkbox" class="ArtsAndCulture" value="Glass Arts"/> Glass Arts<br>
            <input type="checkbox" class="ArtsAndCulture" value="Interpretive History"/> Interpretive History<br>
            <input type="checkbox" class="ArtsAndCulture" value="Literacy Arts"/> Literacy Arts<br>
            <input type="checkbox" class="ArtsAndCulture" value="Media Arts"/> Media Arts<br>
            <input type="checkbox" class="ArtsAndCulture" value="Music: Choral"/> Music: Choral<br>
            <input type="checkbox" class="ArtsAndCulture" value="Music: Instrumental"/> Music: Instrumental<br>
            <input type="checkbox" class="ArtsAndCulture" value="Painting"/> Painting<br>
            <input type="checkbox" class="ArtsAndCulture" value="Performing Arts"/> Performing Arts<br>
            <input type="checkbox" class="ArtsAndCulture" value="Photography"/> Photography<br>
            <input type="checkbox" class="ArtsAndCulture" value="Poetry/Spoken Word"/> Poetry/Spoken Word<br>
            <input type="checkbox" class="ArtsAndCulture" value="Printmaking"/> Printmaking<br>
            <input type="checkbox" class="ArtsAndCulture" value="Puppetry"/> Puppetry<br>
            <input type="checkbox" class="ArtsAndCulture" value="Radio/Audio Production"/> Radio/Audio Production<br>
            <input type="checkbox" class="ArtsAndCulture" value="Sculpture"/> Sculpture<br>
            <input type="checkbox" class="ArtsAndCulture" value="Theater"/> Theater<br>
            <input type="checkbox" class="ArtsAndCulture" value="Visual Arts"/> Visual Arts<br>
            <input type="checkbox" class="ArtsAndCulture" value="Jazz"/> Jazz<br>
            <input type="checkbox" class="ArtsAndCulture" value="Vocal Music"/> Vocal Music<br>
            <input type="checkbox" class="ArtsAndCulture" value="STEAM"/> STEAM<br>
            <input type="checkbox" class="ArtsAndCulture" value="Modern Dance"/> Modern Dance<br>
            <input type="checkbox" class="ArtsAndCulture" value="Ballet"/> Ballet<br>
            <input type="checkbox" class="ArtsAndCulture" value="West African Dance"/> West African Dance<br>
            <input type="checkbox" class="ArtsAndCulture" value="Ballroom Dance"/> Ballroom Dance<br>
            <input type="checkbox" class="ArtsAndCulture" value="Cultural/World Dance"/> Cultural/World Dance<br>
            <input type="checkbox" class="ArtsAndCulture" value="Liturgical Dance"/> Liturgical Dance<br>
            <input type="checkbox" class="ArtsAndCulture" value="Tap Dance"/> Tap Dance<br>
            <input type="checkbox" class="ArtsAndCulture" value="Hip Hop"/> Hip Hop<br>
            <input type="checkbox" class="ArtsAndCulture" value="Drumming"/> Drumming<br>
            <input type="checkbox" class="ArtsAndCulture" value="Acting"/> Acting<br>
            <input type="checkbox" class="ArtsAndCulture" value="Musical Theatre"/> Musical Theatre<br>
            <input type="checkbox" class="ArtsAndCulture" value="Storytelling"/> Storytelling<br>
            <input type="checkbox" class="ArtsAndCulture" value="Music Production"/> Music Production<br>
            <input type="checkbox" class="ArtsAndCulture" value="Mural"/> Mural<br> 
            <button class="filterCheck" id="artsCheck"> Check All </button>
            <button class="filterUncheck" id="artsUncheck"> Uncheck All </button>
        </div>

        <button class="accordion" @click="showEnvironment = !showEnvironment">Environment</button>
        <div class="panel" v-if="showEnvironment">
            <input type="checkbox" class="Environment" value="Agriculture/Farming"/> Agriculture/ Farming<br>
            <input type="checkbox" class="Environment" value="Air quality"/> Air quality<br>
            <input type="checkbox" class="Environment" value="Biodiversity"/> Biodiversity<br>
            <input type="checkbox" class="Environment" value="Climate Change"/> Climate Change<br>
            <input type="checkbox" class="Environment" value="Ecosystems"/> Ecosystems<br>
            <input type="checkbox" class="Environment" value="Energy"/> Energy<br>
            <input type="checkbox" class="Environment" value="Environmental Health"/> Environmental Health<br>
            <input type="checkbox" class="Environment" value="Environmental Justice"/> Environmental Justice<br>
            <input type="checkbox" class="Environment" value="Environmental Science"/> Environmental Science<br>
            <input type="checkbox" class="Environment" value="Forestry"/> Forestry (urban focus)<br>
            <input type="checkbox" class="Environment" value="Horticulture/Gardening"/> Horticulture/Gardening<br>
            <input type="checkbox" class="Environment" value="Natural Resources/ Resource Management"/> Natural Resources/Resource Management<br>
            <input type="checkbox" class="Environment" value="Nature/Wildlife"/> Nature/Wildlife<br>
            <input type="checkbox" class="Environment" value="Pollution prevention"/> Pollution prevention<br>
            <input type="checkbox" class="Environment" value="Recycling/waste management"/> Recycling/waste management<br>
            <input type="checkbox" class="Environment" value="Schoolyard Ecology"/> Schoolyard Ecology<br>
            <input type="checkbox" class="Environment" value="Sustainable Development"/> Sustainable Development<br>
            <input type="checkbox" class="Environment" value="Transportation"/> Transportation<br>
            <input type="checkbox" class="Environment" value="Unspecified Environment"/> Unspecified Environment<br>
            <input type="checkbox" class="Environment" value="Urban Environment/Ecology"/> Urban Environment/Ecology<br>
            <input type="checkbox" class="Environment" value="Water Resources"/> Water Resources<br>
            <button class="filterCheck" id="environmentCheck"> Check All </button>
            <button class="filterUncheck" id="environmentUncheck"> Uncheck All </button>
        </div>

        <button class="accordion" @click="showSports = !showSports">Sports and Recreation</button>
        <div class="panel" v-if="showSports">
            <input type="checkbox" class="SportsAndRecreation" value="Aerobics"/> Aerobics<br>
            <input type="checkbox" class="SportsAndRecreation" value="Baseball"/> Baseball<br>
            <input type="checkbox" class="SportsAndRecreation" value="Basketball"/> Basketball<br>
            <input type="checkbox" class="SportsAndRecreation" value="Boxing"/> Boxing<br>
            <input type="checkbox" class="SportsAndRecreation" value="Cheerleading"/> Cheerleading<br>
            <input type="checkbox" class="SportsAndRecreation" value="Crew/Rowing"/> Crew/Rowing<br>
            <input type="checkbox" class="SportsAndRecreation" value="Cycling"/> Cycling<br>
            <input type="checkbox" class="SportsAndRecreation" value="Dance/Gymnastics"/> Dance/Gymnastics<br>
            <input type="checkbox" class="SportsAndRecreation" value="Dodgeball"/> Dodgeball<br>
            <input type="checkbox" class="SportsAndRecreation" value="Double Dutch/ Jump Rope"/> Double Dutch/ Jump Rope<br>
            <input type="checkbox" class="SportsAndRecreation" value="Football"/> Football<br>
            <input type="checkbox" class="SportsAndRecreation" value="Golf"/> Golf<br>
            <input type="checkbox" class="SportsAndRecreation" value="Hockey/ Skating"/> Hockey/Skating<br>
            <input type="checkbox" class="SportsAndRecreation" value="Kayaking"/> Kayaking<br>
            <input type="checkbox" class="SportsAndRecreation" value="Kickboxing"/> Kickboxing<br>
            <input type="checkbox" class="SportsAndRecreation" value="Lacrosse"/> Lacrosse<br>
            <input type="checkbox" class="SportsAndRecreation" value="Martial Arts"/> Martial Arts<br>
            <input type="checkbox" class="SportsAndRecreation" value="Open Gym"/> Open Gym<br>
            <input type="checkbox" class="SportsAndRecreation" value="Outdoor Adventure"/> Outdoor Adventure<br>
            <input type="checkbox" class="SportsAndRecreation" value="Rock Climbing"/> Rock Climbing<br>
            <input type="checkbox" class="SportsAndRecreation" value="Ropes Course"/> Ropes Course<br>
            <input type="checkbox" class="SportsAndRecreation" value="Rugby"/> Rugby<br>
            <input type="checkbox" class="SportsAndRecreation" value="Running/ Cross Country"/> Running/Cross Country<br>
            <input type="checkbox" class="SportsAndRecreation" value="Sailing"/> Sailing<br>
            <input type="checkbox" class="SportsAndRecreation" value="Skiing/Snowboarding"/> Skiing/Snowboarding<br>
            <input type="checkbox" class="SportsAndRecreation" value="Soccer"/> Soccer<br>
            <input type="checkbox" class="SportsAndRecreation" value="Softball"/> Softball<br>
            <input type="checkbox" class="SportsAndRecreation" value="Strength/Conditioning"/> Strength/Conditioning<br>
            <input type="checkbox" class="SportsAndRecreation" value="Swimming"/> Swimming<br>
            <input type="checkbox" class="SportsAndRecreation" value="Tball"/> Tball<br>
            <input type="checkbox" class="SportsAndRecreation" value="Tennis/Squash"/> Tennis/Squash<br>
            <input type="checkbox" class="SportsAndRecreation" value="Track and Field"/> Track and Field<br>
            <input type="checkbox" class="SportsAndRecreation" value="Unspecified Sport"/> Unspecified Sport<br>
            <input type="checkbox" class="SportsAndRecreation" value="Volleyball"/> Volleyball<br>
            <input type="checkbox" class="SportsAndRecreation" value="Yoga/Pilates"/> Yoga/Pilates<br>
            <input type="checkbox" class="SportsAndRecreation" value="Wrestling"/> Wrestling<br>
            <button class="filterCheck" id="sportsCheck"> Check All </button>
            <button class="filterUncheck" id="sportsUncheck"> Uncheck All </button>
        </div>

        <button class="accordion" @click="showTech = !showTech">Technology/ Media Literacy</button>
        <div class="panel" v-if="showTech">
            <input type="checkbox" class="TechnologyMediaLiteracy" value="Computer Literacy"/> Computer Literacy<br>
            <input type="checkbox" class="TechnologyMediaLiteracy" value="Computer Programming"/> Computer Programming<br>
            <input type="checkbox" class="TechnologyMediaLiteracy" value="Graphic Design"/> Graphic Design<br>
            <input type="checkbox" class="TechnologyMediaLiteracy" value="Media Literacy"/> Media Literacy<br>
            <input type="checkbox" class="TechnologyMediaLiteracy" value="Technology"/> Technology<br>
            <input type="checkbox" class="TechnologyMediaLiteracy" value="Video Game Design"/> Video Game Design<br>
            <input type="checkbox" class="TechnologyMediaLiteracy" value="Web Design"/> Web Design<br>
            <button class="filterCheck" id="technologyCheck"> Check All </button>
            <button class="filterUncheck" id="technologyUncheck"> Uncheck All </button>
        </div>

        <button class="accordion" @click="showEarlyEd = !showEarlyEd">Early Education</button>
        <div class="panel" v-if="showEarlyEd">
            <input type="checkbox" class="EarlyEducation" value="Early Literacy and Reading"/> Early Literacy and Reading<br>
            <input type="checkbox" class="EarlyEducation" value="Parent Child Enrichment"/> Parent Child Enrichment<br>
            <input type="checkbox" class="EarlyEducation" value="Play groups"/> Play groups<br>
            <input type="checkbox" class="EarlyEducation" value="Play-based learning"/> Play-based learning<br>
            <input type="checkbox" class="EarlyEducation" value="School Aged Child care"/> School Aged Child care<br>
            <input type="checkbox" class="EarlyEducation" value="Story Time"/> Story Time<br>
            <button class="filterCheck" id="educationCheck"> Check All </button>
            <button class="filterUncheck" id="educationUncheck"> Uncheck All </button>
        </div>

        <button class="accordion" @click="showJobs = !showJobs">Jobs/Career Exploration</button>
        <div class="panel" v-if="showJobs">
            <input type="checkbox" class="JobsCareerExploration" value="Career Development"/> Career Development<br>
            <input type="checkbox" class="JobsCareerExploration" value="Employment Exploration"/> Employment Exploration<br>
            <input type="checkbox" class="JobsCareerExploration" value="Entrepreneurship"/> Entrepreneurship<br>
            <input type="checkbox" class="JobsCareerExploration" value="Job Shadowing"/> Job Shadowing<br>
            <input type="checkbox" class="JobsCareerExploration" value="Job Skills"/> Job Skills<br>
            <input type="checkbox" class="JobsCareerExploration" value="Paid employment"/> Paid employment<br>
            <input type="checkbox" class="JobsCareerExploration" value="Resume building"/> Resume building<br>
            <input type="checkbox" class="JobsCareerExploration" value="Unpaid Internship"/> Unpaid Internship<br>
            <input type="checkbox" class="JobsCareerExploration" value="Volunteer Opportunity"/> Volunteer Opportunity<br>
            <button class="filterCheck" id="jobsCheck"> Check All </button>
            <button class="filterUncheck" id="jobsUncheck"> Uncheck All </button>
        </div>

        <button class="accordion" @click="showCommunity = !showCommunity">Community Service/ Civic Engagement</button>
        <div class="panel" v-if="showCommunity">
            <input type="checkbox" class="CommunityServiceCivicEngagement" value="Civic engagement"/> Civic engagement<br>
            <input type="checkbox" class="CommunityServiceCivicEngagement" value="Community service"/> Community service<br>
            <input type="checkbox" class="CommunityServiceCivicEngagement" value="Philanthropy"/> Philanthropy<br>
            <input type="checkbox" class="CommunityServiceCivicEngagement" value="Service Learning"/> Service Learning<br>
            <input type="checkbox" class="CommunityServiceCivicEngagement" value="Social justice"/> Social justice<br>
            <input type="checkbox" class="CommunityServiceCivicEngagement" value="Youth organizing"/> Youth organizing<br>
            <button class="filterCheck" id="communityCheck"> Check All </button>
            <button class="filterUncheck" id="communityUncheck"> Uncheck All </button>
        </div>

        <button class="accordion" @click="showYouth = !showYouth">Youth Development</button>
        <div class="panel" v-if="showYouth">
            <input type="checkbox" class="YouthDevelopment" value="Alumni Services"/> Alumni Services<br>
            <input type="checkbox" class="YouthDevelopment" value="Communication Skills"/> Communication Skills<br>
            <input type="checkbox" class="YouthDevelopment" value="Conflict Resolution"/> Conflict Resolution<br>
            <input type="checkbox" class="YouthDevelopment" value="Field Trips"/> Field Trips<br>
            <input type="checkbox" class="YouthDevelopment" value="Leadership Development"/> Leadership Development<br>
            <input type="checkbox" class="YouthDevelopment" value="Life-Skills"/> Life-Skills<br>
            <input type="checkbox" class="YouthDevelopment" value="Mentoring"/> Mentoring<br>
            <input type="checkbox" class="YouthDevelopment" value="Problem-Solving"/> Problem-Solving<br>
            <input type="checkbox" class="YouthDevelopment" value="21st Century Skills"/> 21st Century Skills<br>
            <input type="checkbox" class="YouthDevelopment" value="Self-Esteem"/> Self-Esteem<br>
            <input type="checkbox" class="YouthDevelopment" value="Social Skills"/> Social Skills<br>
            <input type="checkbox" class="YouthDevelopment" value="Team Building"/> Team Building<br>
            <button class="filterCheck" id="youthCheck"> Check All </button>
            <button class="filterUncheck" id="youthUncheck"> Uncheck All </button>
        </div>

        <button class="accordion" @click="showCollege = !showCollege">College Readiness</button>
        <div class="panel" v-if="showCollege">
            <input type="checkbox" class="CollegeReadiness" value="College Counseling"/> College Counseling<br>
            <input type="checkbox" class="CollegeReadiness" value="College Prep"/> College Prep<br>
            <input type="checkbox" class="CollegeReadiness" value="College Readiness"/> College Readiness<br>
            <input type="checkbox" class="CollegeReadiness" value="Financial Counseling"/> Financial Counseling<br>
            <button class="filterCheck" id="collegeCheck"> Check All </button>
            <button class="filterUncheck" id="collegeUncheck"> Uncheck All </button>
        </div>

        <button class="accordion" @click="showHealth = !showHealth">Health</button>
        <div class="panel" v-if="showHealth">
            <input type="checkbox" class="Health" value="Asthma"/> Asthma<br>
            <input type="checkbox" class="Health" value="Bereavement/Greif Work"/> Bereavement/Greif Work<br>
            <input type="checkbox" class="Health" value="Bike Safety"/> Bike Safety<br>
            <input type="checkbox" class="Health" value="Case Management"/> Case Management<br>
            <input type="checkbox" class="Health" value="Counseling"/> Counseling<br>
            <input type="checkbox" class="Health" value="Diabetes"/> Diabetes<br>
            <input type="checkbox" class="Health" value="HIV/Aids Prevention"/> HIV/Aids Prevention<br>
            <input type="checkbox" class="Health" value="Hygiene"/> Hygiene<br>
            <input type="checkbox" class="Health" value="Mental Health"/> Mental Health<br>
            <input type="checkbox" class="Health" value="Nutrition"/> Nutrition<br>
            <input type="checkbox" class="Health" value="Physical Fitness"/> Physical Fitness<br>
            <input type="checkbox" class="Health" value="Sexual Education/Sexuality"/> Sexual Education/Sexuality<br>
            <input type="checkbox" class="Health" value="Stress Management"/> Stress Management<br>
            <input type="checkbox" class="Health" value="Substance Abuse Prevention"/> Substance Abuse Prevention<br>
            <input type="checkbox" class="Health" value="Trauma Work"/> Trauma Work<br>
            <input type="checkbox" class="Health" value="Unspecified Health"/> Unspecified Health<br>
            <input type="checkbox" class="Health" value="Violence Prevention"/> Violence Prevention<br>
            <input type="checkbox" class="Health" value="Weight Management"/> Weight Management<br>
            <button class="filterCheck" id="healthCheck"> Check All </button>
            <button class="filterUncheck" id="healthUncheck"> Uncheck All </button>
        </div>

        <button class="accordion" @click="showFaith = !showFaith">Faith-Based/ Spirituality</button>
        <div class="panel" v-if="showFaith">
            <input type="checkbox" class="FaithBasedSpirituality" value="Faith-Based/ Spirituality"/> Faith-Based/ Spirituality<br>
        </div>
    </div>
</template>

<script>
export default {
  data() {
      return {
          showAcademic: false,
          showArts: false,
          showEnvironment: false,
          showSports: false,
          showTech: false,
          showEarlyEd: false,
          showJobs: false,
          showCommunity: false,
          showYouth: false,
          showCollege: false,
          showHealth: false,
          showFaith: false
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

.panel {
    padding: 0;
    background-color: white;
    max-height: 900px;
    overflow: hidden;
    /*transition: 0.6s ease-in-out;*/
}
</style>
