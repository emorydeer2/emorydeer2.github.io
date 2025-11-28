# emorydeer2.github.io<!DOCTYPE html>
<!-- saved from url=(0106)https://epfc-skill-planner.pages.dev/?skills=19426039812110622663804760752509063989821440&combat=537755908 -->
<html><head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
    <style id="__________cytoscape_stylesheet">.__________cytoscape_container { position: relative; }</style><link rel="stylesheet" href="./EPFC Skill planner_files/styles.css">

    <script src="./EPFC Skill planner_files/cytoscape.min.js.download"></script>

    <title>EPFC Skill planner</title>
    <meta content="EPFC Skill planner" property="og:title">
    <meta content="A webapp to help you plan out your skills" property="og:description">
    <meta content="https://epfc-skill-planner.pages.dev" property="og:url">
    <meta content="https://epfc-skill-planner.pages.dev/auction.png" property="og:image">
    <meta content="#aaaa00" data-react-helmet="true" name="theme-color">
</head>

<body>
    <main class="app-container">
        <div class="tabs">
            <button onclick="switchTab(&#39;skillsContainer&#39;); centerGraph(skillsGraph)" id="skillsTab">Skills</button>
            <button onclick="switchTab(&#39;combatSkillsContainer&#39;); centerGraph(combatSkillsGraph)" id="combatTab">Combat Skills</button>
            <button onclick="switchTab(&#39;inventoryContainer&#39;)" id="inventoryTab">Inventory</button>
            <button onclick="switchTab(&#39;helpContainer&#39;)" id="helpTab">Help</button>
            <button onclick="restart()" id="reset">Reset</button>
        </div>
        <div class="tab-container skills-container hidden" id="skillsContainer">
            <div class="skill-web __________cytoscape_container" id="skill-web" style="-webkit-tap-highlight-color: rgba(0, 0, 0, 0);"><div style="-webkit-tap-highlight-color: rgba(0, 0, 0, 0); position: relative; z-index: 0; overflow: hidden; width: 0px; height: 0px;"><canvas data-id="layer0-selectbox" width="0" height="0" style="user-select: none; -webkit-tap-highlight-color: rgba(0, 0, 0, 0); outline-style: none; position: absolute; z-index: 3; width: 0px; height: 0px;"></canvas><canvas data-id="layer1-drag" width="0" height="0" style="user-select: none; -webkit-tap-highlight-color: rgba(0, 0, 0, 0); outline-style: none; position: absolute; z-index: 2; width: 0px; height: 0px;"></canvas><canvas data-id="layer2-node" width="0" height="0" style="user-select: none; -webkit-tap-highlight-color: rgba(0, 0, 0, 0); outline-style: none; position: absolute; z-index: 1; width: 0px; height: 0px;"></canvas></div></div>
        </div>
        <div class="tab-container combat-skills-container hidden" id="combatSkillsContainer">
            <div class="combat-skills __________cytoscape_container" id="combatSkills" style="-webkit-tap-highlight-color: rgba(0, 0, 0, 0);"><div style="-webkit-tap-highlight-color: rgba(0, 0, 0, 0); position: relative; z-index: 0; overflow: hidden; width: 0px; height: 0px;"><canvas data-id="layer0-selectbox" width="0" height="0" style="user-select: none; -webkit-tap-highlight-color: rgba(0, 0, 0, 0); outline-style: none; position: absolute; z-index: 3; width: 0px; height: 0px;"></canvas><canvas data-id="layer1-drag" width="0" height="0" style="user-select: none; -webkit-tap-highlight-color: rgba(0, 0, 0, 0); outline-style: none; position: absolute; z-index: 2; width: 0px; height: 0px;"></canvas><canvas data-id="layer2-node" width="0" height="0" style="user-select: none; -webkit-tap-highlight-color: rgba(0, 0, 0, 0); outline-style: none; position: absolute; z-index: 1; width: 0px; height: 0px;"></canvas></div></div>
        </div>
        <div class="tab-container inventory-container hidden" id="inventoryContainer">
            
        </div>
        <div class="tab-container help-container" id="helpContainer">
            <div class="panel">
                <h1>Help &amp; Information</h1>
                <p>You won't find any help here</p>
            </div>
        </div>
        <div class="skill-effects">
            <p>Hold SHIFT to highlight similar skills</p>
            <h1>Stats Overview</h1>
            <h2>Skill points spent: <span id="pointsSpent" class="at-limit">55</span></h2>
            <h2>Combat points spent: <span id="combatPointsSpent" class="at-limit">7</span></h2>
            <p>Health: <span id="health">100</span></p>
            <p>Stamina: <span id="stamina">100</span></p>
            <p>Stamina Regeneration Rate: <span id="staminaRegenRate">15</span>/s</p>
            <p>Stamina Consumption Rate: <span id="staminaConsumptionRate">N/a</span></p>
            <p>Speed: <span id="speed">N/a</span></p>
            <p>Weight: <span id="weight">N/a</span></p>
            <br>
            <p>Dodge Chance: <span id="dodgeChance">30</span>%</p>
            <p>Crit Chance: <span id="critChance">25</span>%</p>
            <p>Reload Speed: <span id="reloadSpeed">150</span>%</p>
            <br>
            <p>Saw/Drill Speed: <span id="appliedForceSpeed">100</span>%</p>
            <p>Lockpicking Speed: <span id="lockpickingSpeed">150</span>%</p>
            <p>Hacking Speed: <span id="hackingSpeed">100</span>%</p>
            <p>Network Resources Usage: <span id="networkResourcesUsage">0.5</span>x</p>
            <p>Tech Item Use Speed: <span id="techUseSpeed">115</span>%</p>
            <br>
            <p>Crouched Detection Speed: <span id="crouchedDetectionSpeed">0.6</span>x</p>
            <p>Suspicious Actions Detection Speed: <span id="suspiciousDetectionSpeed">1</span>x</p>
            <p>Disguised Detection Speed: <span id="disguisedDetectionSpeed">1</span>x</p>
            <p>Camera Detection Speed: <span id="cameraDetectionSpeed">1</span>x</p>
            <br>
            <!--<h1>Encumberance Information</h1>-->
            <!--Not sure if I actually need this lol, will figure out if I do when I get around to items-->
        </div>
    </main>

    <script src="./EPFC Skill planner_files/app.js.download"></script>
    <script src="./EPFC Skill planner_files/tabs.js.download"></script>


<div id="give-freely-root-ejkiikneibegknkgimmihdpcbcedgmpo" class="give-freely-root" data-extension-id="ejkiikneibegknkgimmihdpcbcedgmpo" data-extension-name="Volume Booster" style="display: block;"><template shadowrootmode="open"><style>
  :host {
    all: initial;
  }

  .gf-scroll-remove::-webkit-scrollbar {
    border-radius-bottom-right: 15px;
  }

  button {
    cursor: pointer;
    transition: transform 0.1s ease;
  }

  button:active {
    transform: scale(0.98);
  }

  .give-freely-close-button:hover {
    opacity: 0.7;
  }

  input[type="radio"] {
    margin-right: 8px;
  }

  hr {
    border: none;
    border-top: 1px solid #e5e5e5;
    margin: 1em 0;
  }

  @media (max-width: 600px), (max-height: 480px) {
    #give-freely-checkout-popup {
      display: none !important;
    }
  }
</style><div><div class="gf-app"></div></div></template></div></body></html>
