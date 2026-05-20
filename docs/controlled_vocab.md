---
layout: default
title: "Controlled Vocabulary"
permalink: /controlled_vocab/
---

<style>
  .vocab-intro {
    max-width: 950px;
    line-height: 1.55;
  }

  .vocab-callout {
    border-left: 4px solid #4b8f4b;
    background: #f5faf5;
    padding: 12px 16px;
    margin: 18px 0;
  }

  .vocab-controls {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    margin: 20px 0;
    align-items: center;
  }

  .vocab-controls input,
  .vocab-controls select {
    padding: 8px;
    border: 1px solid #bbb;
    border-radius: 4px;
  }

  .vocab-table-wrapper {
    overflow-x: auto;
  }

  table.vocab-table {
    border-collapse: collapse;
    width: 100%;
    font-size: 0.95rem;
  }

  .vocab-table th {
    position: sticky;
    top: 0;
    background: #f2f2f2;
    border-bottom: 2px solid #ccc;
    text-align: left;
    padding: 8px;
  }

  .vocab-table td {
    border-bottom: 1px solid #ddd;
    vertical-align: top;
    padding: 8px;
  }

  .vocab-table tr:hover {
    background: #fafafa;
  }

  .domain {
    min-width: 150px;
    max-width: 220px;
    white-space: normal;
    font-family: inherit;
    font-size: 0.9rem;
  }

  .term {
    font-weight: 600;
  }

  .small-note {
    font-size: 0.9rem;
    color: #555;
  }
</style>

<h1>Controlled Vocabulary</h1>

<div class="vocab-intro" markdown="0">
  <p>
    This page presents the working controlled vocabulary for the Microbial Biosignatures Project.
    The vocabulary is intended to document the descriptive terms, operational categories, and source
    definitions used in the microbialites database.
  </p>

  <p>
    Many terms are adapted from published microbialite terminology, especially Grey and Awramik (2020),
    while others are operational terms added to support database entry, search, and comparison.
    Definitions marked provisional should be treated as working definitions open to revision.
  </p>

  <div class="vocab-callout">
    <strong>Current status:</strong> preliminary working vocabulary. Terms and definitions are being
    reviewed as the database structure and community feedback evolve.
  </div>

  <p class="small-note">
    Columns shown below include the category, term, working definition, source information, status, and notes.
  </p>
</div>

<div class="vocab-controls" markdown="0">
  <input type="text" id="vocabSearch" placeholder="Search terms, categories, definitions, or sources..." onkeyup="filterVocab()" style="min-width: 320px;">
  <select id="domainFilter" onchange="filterVocab()">
    <option value="">All categories</option>
    <option value="tlkpitemtype">item type</option>
    <option value="tlkpmacroaspectratio">macrostructure, aspect ratio</option>
    <option value="tlkpmacroattitude">macrostructure, attitude</option>
    <option value="tlkpmacrobranchingmode">macrostructure, branching mode</option>
    <option value="tlkpmacrobranchingstyle">macrostructure, branching style</option>
    <option value="tlkpmacrocolumnshape">macrostructure, column shape</option>
    <option value="tlkpmacroconicalshapes">macrostructure, conical shapes</option>
    <option value="tlkpmacrodivergenceangle">macrostructure, divergence angle</option>
    <option value="tlkpmacrodomeshape">macrostructure, dome shape</option>
    <option value="tlkpmacrogrowthvariability">macrostructure, growth variability</option>
    <option value="tlkpmacrolayershape">macrostructure, layer shape</option>
    <option value="tlkpmacrolinkage">macrostructure, linkage</option>
    <option value="tlkpmacroplanview">macrostructure, plan view</option>
    <option value="tlkpmacroshape">macrostructure, shape</option>
    <option value="tlkpmacrospacing">macrostructure, spacing</option>
    <option value="tlkpmegabedgeometry">megastructure, bed geometry</option>
    <option value="tlkpmegabuildupinterface">megastructure, buildup interface</option>
    <option value="tlkpmegabuilduptype">megastructure, buildup type</option>
    <option value="tlkpmegadepositionalsetting">megastructure, depositional setting</option>
    <option value="tlkpmegahorizontalscale">megastructure, horizontal scale</option>
    <option value="tlkpmegainitiation">megastructure, initiation</option>
    <option value="tlkpmegalat_long_quality">megastructure, latitude/longitude quality</option>
    <option value="tlkpmegalithology">megastructure, lithology</option>
    <option value="tlkpmegamegastructureshape">megastructure, megastructure shape</option>
    <option value="tlkpmegamicrobialitetypes">megastructure, microbialite types</option>
    <option value="tlkpmegasedinterface">megastructure, sediment interface</option>
    <option value="tlkpmegasubstrate">megastructure, substrate</option>
    <option value="tlkpmegaverticalscale">megastructure, vertical scale</option>
    <option value="tlkpmesoalternation">mesostructure, alternation</option>
    <option value="tlkpmesoarchitecture">mesostructure, architecture</option>
    <option value="tlkpmesoclothierarchy">mesostructure, clot hierarchy</option>
    <option value="tlkpmesoclotshape">mesostructure, clot shape</option>
    <option value="tlkpmesograintypes">mesostructure, grain types</option>
    <option value="tlkpmesolaminainheritance">mesostructure, lamina inheritance</option>
    <option value="tlkpmesolampattern">mesostructure, lamina pattern</option>
    <option value="tlkpmesolamprofile">mesostructure, lamina profile</option>
    <option value="tlkpmesolamwaviness">mesostructure, lamina waviness</option>
    <option value="tlkpmesolatcontinuity">mesostructure, lateral continuity</option>
    <option value="tlkpmesomacrolaminae">mesostructure, macrolaminae</option>
    <option value="tlkpmesomodalityskewness">mesostructure, modality skewness</option>
    <option value="tlkpmesooncoidflattening">mesostructure, oncoid flattening</option>
    <option value="tlkpmesooncoids">mesostructure, oncoids</option>
    <option value="tlkpmesooncoidshape">mesostructure, oncoid shape</option>
    <option value="tlkpmesostackingoverlap">mesostructure, stacking overlap</option>
    <option value="tlkpmesosynopticrelief">mesostructure, synoptic relief</option>
    <option value="tlkpmesotypes">mesostructure, types</option>
    <option value="tlkpmesowalls">mesostructure, walls</option>
    <option value="tlkpmicrocarbonategrains">microstructure, carbonate grains</option>
    <option value="tlkpmicrocementtypes">microstructure, cement types</option>
    <option value="tlkpmicroclasticgrains">microstructure, clastic grains</option>
    <option value="tlkpmicromicrofacies">microstructure, microfacies</option>
    <option value="tlkpmicromineralogy">microstructure, mineralogy</option>
    <option value="tlkpmicropercentclastics">microstructure, percent clastics</option>
    <option value="tlkpmicroporositydirection">microstructure, porosity direction</option>
    <option value="tlkpmicroporosityprocess">microstructure, porosity process</option>
    <option value="tlkpmicroporositysize">microstructure, porosity size</option>
    <option value="tlkpmicroporositytypes">microstructure, porosity types</option>
    <option value="tlkpmicrotexturetypes">microstructure, texture types</option>
    <option value="tlkpmicrowentworth">microstructure, Wentworth size class</option>
    <option value="tlkpprojecttectonicsetting">project, tectonic setting</option>
    <option value="tlkpsemandotherdatatypes">SEM and other data types</option>
    <option value="tlkptrait_observation_quality">trait observation quality</option>
  </select>
  <select id="statusFilter" onchange="filterVocab()">
    <option value="">All statuses</option>
    <option value="accepted">accepted</option>
    <option value="obsolete">obsolete</option>
    <option value="provisional">provisional</option>
  </select>
</div>

<div class="vocab-table-wrapper" markdown="0">
  <table class="vocab-table" id="vocabTable">
    <thead>
      <tr>
        <th>Category</th>
        <th>Term</th>
        <th>Definition</th>
        <th>Source</th>
        <th>Status</th>
        <th>Notes</th>
      </tr>
    </thead>
    <tbody>
    <tr data-domain="tlkpitemtype" data-status="accepted">
      <td class="domain">item type</td>
      <td class="term">Journal Article</td>
      <td>Article published in a peer-reviewed academic journal</td>
      <td>Database operational terminology</td>
      <td>accepted</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpitemtype" data-status="accepted">
      <td class="domain">item type</td>
      <td class="term">Unpublished Work</td>
      <td>Creative or scholarly work not formally published or distributed</td>
      <td>Database operational terminology</td>
      <td>accepted</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpitemtype" data-status="accepted">
      <td class="domain">item type</td>
      <td class="term">Slide Presentation</td>
      <td>Presentation consisting primarily of visual slides or projected material</td>
      <td>Database operational terminology</td>
      <td>accepted</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpitemtype" data-status="accepted">
      <td class="domain">item type</td>
      <td class="term">Report</td>
      <td>Formal document presenting findings, data, or institutional information</td>
      <td>Database operational terminology</td>
      <td>accepted</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpitemtype" data-status="accepted">
      <td class="domain">item type</td>
      <td class="term">Newspaper Article</td>
      <td>Article published in a newspaper or news periodical</td>
      <td>Database operational terminology</td>
      <td>accepted</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpitemtype" data-status="accepted">
      <td class="domain">item type</td>
      <td class="term">Map</td>
      <td>Cartographic document representing geographic information</td>
      <td>Database operational terminology</td>
      <td>accepted</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpitemtype" data-status="accepted">
      <td class="domain">item type</td>
      <td class="term">Generic</td>
      <td>General or miscellaneous reference type not fitting other categories</td>
      <td>Database operational terminology</td>
      <td>accepted</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpitemtype" data-status="accepted">
      <td class="domain">item type</td>
      <td class="term">Artwork</td>
      <td>Creative work or visual media item including paintings, illustrations, or sculptures</td>
      <td>Database operational terminology</td>
      <td>accepted</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpitemtype" data-status="accepted">
      <td class="domain">item type</td>
      <td class="term">Bill</td>
      <td>Legislative or proposed legal document introduced for consideration</td>
      <td>Database operational terminology</td>
      <td>accepted</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpitemtype" data-status="accepted">
      <td class="domain">item type</td>
      <td class="term">Blog Post</td>
      <td>Informal online publication typically presented in reverse chronological order</td>
      <td>Database operational terminology</td>
      <td>accepted</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpitemtype" data-status="accepted">
      <td class="domain">item type</td>
      <td class="term">Case</td>
      <td>Published legal decision or judicial proceeding</td>
      <td>Database operational terminology</td>
      <td>accepted</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpitemtype" data-status="accepted">
      <td class="domain">item type</td>
      <td class="term">Book</td>
      <td>Standalone published written work issued as a complete volume</td>
      <td>Database operational terminology</td>
      <td>accepted</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpitemtype" data-status="accepted">
      <td class="domain">item type</td>
      <td class="term">Computer Program</td>
      <td>Software application, script, or executable digital tool</td>
      <td>Database operational terminology</td>
      <td>accepted</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpitemtype" data-status="accepted">
      <td class="domain">item type</td>
      <td class="term">Hearing</td>
      <td>Formal proceeding or session conducted by a legislative or judicial body</td>
      <td>Database operational terminology</td>
      <td>accepted</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpitemtype" data-status="accepted">
      <td class="domain">item type</td>
      <td class="term">In Press</td>
      <td>Work accepted for publication but not yet formally published</td>
      <td>Database operational terminology</td>
      <td>accepted</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpitemtype" data-status="accepted">
      <td class="domain">item type</td>
      <td class="term">Music</td>
      <td>Musical composition, recording, or performance work</td>
      <td>Database operational terminology</td>
      <td>accepted</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpitemtype" data-status="accepted">
      <td class="domain">item type</td>
      <td class="term">Patent</td>
      <td>Legally recognized intellectual property filing protecting an invention</td>
      <td>Database operational terminology</td>
      <td>accepted</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpitemtype" data-status="accepted">
      <td class="domain">item type</td>
      <td class="term">Statute</td>
      <td>Written law formally enacted by a governing authority</td>
      <td>Database operational terminology</td>
      <td>accepted</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpitemtype" data-status="accepted">
      <td class="domain">item type</td>
      <td class="term">Video</td>
      <td>Recorded moving-image media item</td>
      <td>Database operational terminology</td>
      <td>accepted</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpitemtype" data-status="accepted">
      <td class="domain">item type</td>
      <td class="term">Book Chapter</td>
      <td>Individually authored section or chapter within a larger edited book</td>
      <td>Database operational terminology</td>
      <td>accepted</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpitemtype" data-status="accepted">
      <td class="domain">item type</td>
      <td class="term">Conference Paper</td>
      <td>Paper or abstract presented at a professional or academic conference</td>
      <td>Database operational terminology</td>
      <td>accepted</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpitemtype" data-status="accepted">
      <td class="domain">item type</td>
      <td class="term">Electronic Article</td>
      <td>Article published in an electronic-only or primarily online format</td>
      <td>Database operational terminology</td>
      <td>accepted</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpitemtype" data-status="accepted">
      <td class="domain">item type</td>
      <td class="term">Magazine Article</td>
      <td>Article published in a magazine or popular periodical</td>
      <td>Database operational terminology</td>
      <td>accepted</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpitemtype" data-status="accepted">
      <td class="domain">item type</td>
      <td class="term">Manuscript</td>
      <td>Unpublished written document or draft work</td>
      <td>Database operational terminology</td>
      <td>accepted</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpitemtype" data-status="accepted">
      <td class="domain">item type</td>
      <td class="term">Thesis/Dissertation</td>
      <td>Academic thesis or dissertation submitted for a degree</td>
      <td>Database operational terminology</td>
      <td>accepted</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpitemtype" data-status="accepted">
      <td class="domain">item type</td>
      <td class="term">Web Page</td>
      <td>Online document or content accessed through the web</td>
      <td>Database operational terminology</td>
      <td>accepted</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroaspectratio" data-status="provisional">
      <td class="domain">macrostructure, aspect ratio</td>
      <td class="term">Crustose</td>
      <td>microbialites that are much wider than they are tall; low-relief, sheet-like growth forms.</td>
      <td>Grey and Awramik (2020); p. 83; fig. 78</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroaspectratio" data-status="provisional">
      <td class="domain">macrostructure, aspect ratio</td>
      <td class="term">Stubby</td>
      <td>microbialites with moderate relief; height and width are more comparable, producing short, thick forms.</td>
      <td>Grey and Awramik (2020); p. 83; fig. 78</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroaspectratio" data-status="provisional">
      <td class="domain">macrostructure, aspect ratio</td>
      <td class="term">Slender</td>
      <td>microbialites that are significantly taller than they are wide; narrow, vertically elongate forms.</td>
      <td>Grey and Awramik (2020); p. 83; fig. 78</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroattitude" data-status="provisional">
      <td class="domain">macrostructure, attitude</td>
      <td class="term">Erect</td>
      <td>Columns or branches grow vertically upward with little deviation from the growth axis.</td>
      <td>Grey and Awramik (2020); p. 102; fig. 86</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroattitude" data-status="provisional">
      <td class="domain">macrostructure, attitude</td>
      <td class="term">Inclined</td>
      <td>Columns or branches consistently lean away from vertical growth.</td>
      <td>Grey and Awramik (2020); p. 102; fig. 86</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroattitude" data-status="provisional">
      <td class="domain">macrostructure, attitude</td>
      <td class="term">Prostrate</td>
      <td>Microbialites grow laterally along or close to the substrate surface.</td>
      <td>Grey and Awramik (2020); p. 102; fig. 86</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroattitude" data-status="provisional">
      <td class="domain">macrostructure, attitude</td>
      <td class="term">Pendant</td>
      <td>Structures hang downward from an overhanging surface or cavity roof.</td>
      <td>Grey and Awramik (2020); p. 102; fig. 86</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroattitude" data-status="provisional">
      <td class="domain">macrostructure, attitude</td>
      <td class="term">Sinuous</td>
      <td>Growth form follows a curving or winding path rather than remaining straight.</td>
      <td>Grey and Awramik (2020); p. 102; fig. 86</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroattitude" data-status="provisional">
      <td class="domain">macrostructure, attitude</td>
      <td class="term">Hyponastic</td>
      <td>Branches or laminae curve downward during growth.</td>
      <td>Grey and Awramik (2020); p. 102; fig. 86</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroattitude" data-status="provisional">
      <td class="domain">macrostructure, attitude</td>
      <td class="term">Epinastic</td>
      <td>Branches or laminae curve upward during growth.</td>
      <td>Grey and Awramik (2020); p. 102; fig. 86</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroattitude" data-status="provisional">
      <td class="domain">macrostructure, attitude</td>
      <td class="term">Encapsulated</td>
      <td>Growth forms are partly or completely enclosed by later surrounding growth.</td>
      <td>Grey and Awramik (2020); p. 102; fig. 86</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrobranchingmode" data-status="provisional">
      <td class="domain">macrostructure, branching mode</td>
      <td class="term">Alpha</td>
      <td>Branches diverge directly from a parent branch while maintaining general upward growth.</td>
      <td>Grey and Awramik (2020); p. 112; fig. 96</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrobranchingmode" data-status="provisional">
      <td class="domain">macrostructure, branching mode</td>
      <td class="term">Beta</td>
      <td>Secondary branches arise laterally from existing branches at distinct angles.</td>
      <td>Grey and Awramik (2020); p. 112; fig. 96</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrobranchingmode" data-status="provisional">
      <td class="domain">macrostructure, branching mode</td>
      <td class="term">Gamma</td>
      <td>Complex repeated branching produces highly subdivided or bushy forms.</td>
      <td>Grey and Awramik (2020); p. 112; fig. 96</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrobranchingstyle" data-status="provisional">
      <td class="domain">macrostructure, branching style</td>
      <td class="term">Bifurcate</td>
      <td>Branches divide into two daughter branches.</td>
      <td>Grey and Awramik (2020); p. 108; fig. 92</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrobranchingstyle" data-status="provisional">
      <td class="domain">macrostructure, branching style</td>
      <td class="term">Multifurcate</td>
      <td>Branches divide into multiple daughter branches from a single point.</td>
      <td>Grey and Awramik (2020); p. 108; fig. 92</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrobranchingstyle" data-status="provisional">
      <td class="domain">macrostructure, branching style</td>
      <td class="term">Dichotomous</td>
      <td>Repeated equal splitting produces paired branching patterns.</td>
      <td>Grey and Awramik (2020); p. 108; fig. 92</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrobranchingstyle" data-status="provisional">
      <td class="domain">macrostructure, branching style</td>
      <td class="term">Lateral</td>
      <td>Secondary branches emerge from the sides of main branches.</td>
      <td>Grey and Awramik (2020); p. 108; fig. 92</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrobranchingstyle" data-status="provisional">
      <td class="domain">macrostructure, branching style</td>
      <td class="term">Coalesced</td>
      <td>Adjacent branches grow together or merge along portions of their margins.</td>
      <td>Grey and Awramik (2020); p. 108; fig. 92</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrobranchingstyle" data-status="provisional">
      <td class="domain">macrostructure, branching style</td>
      <td class="term">Anastomosed</td>
      <td>Branches reconnect after separation to form network-like interconnections.</td>
      <td>Grey and Awramik (2020); p. 108; fig. 92</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrocolumnshape" data-status="provisional">
      <td class="domain">macrostructure, column shape</td>
      <td class="term">Cylindrical</td>
      <td>Columns maintain a nearly constant diameter through most of their height.</td>
      <td>Grey and Awramik (2020); p. 77; fig. 61</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrocolumnshape" data-status="provisional">
      <td class="domain">macrostructure, column shape</td>
      <td class="term">Terete</td>
      <td>Columns are rounded and rod-like with relatively uniform diameter.</td>
      <td>Grey and Awramik (2020); p. 77; fig. 61</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrocolumnshape" data-status="provisional">
      <td class="domain">macrostructure, column shape</td>
      <td class="term">Turbinate</td>
      <td>Columns widen upward or outward from a narrower base.</td>
      <td>Grey and Awramik (2020); p. 77; fig. 61</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroconicalshapes" data-status="provisional">
      <td class="domain">macrostructure, conical shapes</td>
      <td class="term">Collared conical</td>
      <td>Cones possess collar-like outward flanges or rims.</td>
      <td>Grey and Awramik (2020); p. 77; fig. 66</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroconicalshapes" data-status="provisional">
      <td class="domain">macrostructure, conical shapes</td>
      <td class="term">Petaloid conical</td>
      <td>Cones develop petal-like outward lobes or subdivisions.</td>
      <td>Grey and Awramik (2020); p. 77; fig. 66</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroconicalshapes" data-status="provisional">
      <td class="domain">macrostructure, conical shapes</td>
      <td class="term">Simple</td>
      <td>Cone forms are simple and unmodified with smooth converging sides.</td>
      <td>Grey and Awramik (2020); p. 77; fig. 66</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroconicalshapes" data-status="provisional">
      <td class="domain">macrostructure, conical shapes</td>
      <td class="term">Cylindrical</td>
      <td>Cones maintain a relatively constant diameter through much of their height.</td>
      <td>Grey and Awramik (2020); p. 77; fig. 66</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroconicalshapes" data-status="provisional">
      <td class="domain">macrostructure, conical shapes</td>
      <td class="term">Concave</td>
      <td>Cone sides curve inward to produce a depressed or inward-bowing profile.</td>
      <td>Grey and Awramik (2020); p. 77; fig. 66</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroconicalshapes" data-status="provisional">
      <td class="domain">macrostructure, conical shapes</td>
      <td class="term">Convex</td>
      <td>Cone sides bulge outward to produce an outward-bowing profile.</td>
      <td>Grey and Awramik (2020); p. 77; fig. 66</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroconicalshapes" data-status="provisional">
      <td class="domain">macrostructure, conical shapes</td>
      <td class="term">Terete</td>
      <td>Cones are rod-like and rounded in overall form.</td>
      <td>Grey and Awramik (2020); p. 77; fig. 66</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroconicalshapes" data-status="provisional">
      <td class="domain">macrostructure, conical shapes</td>
      <td class="term">Inclined</td>
      <td>Cones lean consistently away from vertical orientation.</td>
      <td>Grey and Awramik (2020); p. 77; fig. 66</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroconicalshapes" data-status="provisional">
      <td class="domain">macrostructure, conical shapes</td>
      <td class="term">Ridged conical</td>
      <td>Cones possess longitudinal ridges extending along the cone surface.</td>
      <td>Grey and Awramik (2020); p. 77; fig. 66</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroconicalshapes" data-status="provisional">
      <td class="domain">macrostructure, conical shapes</td>
      <td class="term">Branched conical</td>
      <td>Cones display repeated branching or subdivision during growth.</td>
      <td>Grey and Awramik (2020); p. 77; fig. 66</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrodivergenceangle" data-status="provisional">
      <td class="domain">macrostructure, divergence angle</td>
      <td class="term">Parallel</td>
      <td>Branches remain nearly parallel with minimal outward spreading.</td>
      <td>Grey and Awramik (2020); p. 102; fig. 99</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrodivergenceangle" data-status="provisional">
      <td class="domain">macrostructure, divergence angle</td>
      <td class="term">Moderate Divergence</td>
      <td>Branches diverge outward at moderate angles from the main growth direction.</td>
      <td>Grey and Awramik (2020); p. 102; fig. 99</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrodivergenceangle" data-status="provisional">
      <td class="domain">macrostructure, divergence angle</td>
      <td class="term">Marked Divergence</td>
      <td>Branches diverge strongly outward from the main growth direction.</td>
      <td>Grey and Awramik (2020); p. 102; fig. 99</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrodivergenceangle" data-status="provisional">
      <td class="domain">macrostructure, divergence angle</td>
      <td class="term">Horizontal Divergence</td>
      <td>Branches diverge outward to nearly horizontal orientations.</td>
      <td>Grey and Awramik (2020); p. 102; fig. 99</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrodomeshape" data-status="provisional">
      <td class="domain">macrostructure, dome shape</td>
      <td class="term">Hemispherical</td>
      <td>Domes form smooth half-spherical shapes with broadly curved surfaces.</td>
      <td>Grey and Awramik (2020); p. 77; fig. 61</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrodomeshape" data-status="provisional">
      <td class="domain">macrostructure, dome shape</td>
      <td class="term">Bulbous</td>
      <td>Domes are swollen or inflated with rounded outward expansion.</td>
      <td>Grey and Awramik (2020); p. 77; fig. 61</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrodomeshape" data-status="provisional">
      <td class="domain">macrostructure, dome shape</td>
      <td class="term">Nodular</td>
      <td>Domes consist of rounded nodules or knobby protrusions.</td>
      <td>Grey and Awramik (2020); p. 77; fig. 61</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrogrowthvariability" data-status="provisional">
      <td class="domain">macrostructure, growth variability</td>
      <td class="term">Uniform</td>
      <td>Growth maintains relatively consistent size and form through development.</td>
      <td>Grey and Awramik (2020); p. 98; fig. 82</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrogrowthvariability" data-status="provisional">
      <td class="domain">macrostructure, growth variability</td>
      <td class="term">Constringed</td>
      <td>Growth repeatedly narrows or pinches inward along its length.</td>
      <td>Grey and Awramik (2020); p. 98; fig. 82</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrogrowthvariability" data-status="provisional">
      <td class="domain">macrostructure, growth variability</td>
      <td class="term">Ragged</td>
      <td>Growth margins are irregular, uneven, or highly variable in outline.</td>
      <td>Grey and Awramik (2020); p. 98; fig. 82</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrolayershape" data-status="provisional">
      <td class="domain">macrostructure, layer shape</td>
      <td class="term">Stratiform</td>
      <td>Growth forms consist of laterally continuous layered sheets.</td>
      <td>Grey and Awramik (2020); p. 74; fig. 58</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrolayershape" data-status="provisional">
      <td class="domain">macrostructure, layer shape</td>
      <td class="term">Undulatory</td>
      <td>Layers display gentle wave-like undulations across the surface.</td>
      <td>Grey and Awramik (2020); p. 74; fig. 58</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrolayershape" data-status="provisional">
      <td class="domain">macrostructure, layer shape</td>
      <td class="term">Pseudo-columnar</td>
      <td>Layered forms begin to develop weak column-like subdivision.</td>
      <td>Grey and Awramik (2020); p. 74; fig. 58</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrolayershape" data-status="provisional">
      <td class="domain">macrostructure, layer shape</td>
      <td class="term">Linked columnar</td>
      <td>Adjacent columns remain connected by continuous laminae.</td>
      <td>Grey and Awramik (2020); p. 74; fig. 58</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrolayershape" data-status="provisional">
      <td class="domain">macrostructure, layer shape</td>
      <td class="term">Linked conical</td>
      <td>Conical forms remain laterally connected by shared laminae.</td>
      <td>Grey and Awramik (2020); p. 74; fig. 58</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrolayershape" data-status="provisional">
      <td class="domain">macrostructure, layer shape</td>
      <td class="term">Linked thrombolitic</td>
      <td>Clotted thrombolitic masses remain laterally interconnected.</td>
      <td>Grey and Awramik (2020); p. 74; fig. 58</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrolinkage" data-status="provisional">
      <td class="domain">macrostructure, linkage</td>
      <td class="term">Linked</td>
      <td>Adjacent microbialite columns or forms are continuously connected to one another.</td>
      <td>Grey and Awramik (2020); p. 63; fig. 46</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrolinkage" data-status="provisional">
      <td class="domain">macrostructure, linkage</td>
      <td class="term">Locally linked</td>
      <td>Connections occur only in limited localized areas between adjacent forms.</td>
      <td>Grey and Awramik (2020); p. 63; fig. 46</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrolinkage" data-status="provisional">
      <td class="domain">macrostructure, linkage</td>
      <td class="term">Sporadically linked</td>
      <td>Connections between adjacent forms occur irregularly and discontinuously.</td>
      <td>Grey and Awramik (2020); p. 63; fig. 46</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrolinkage" data-status="provisional">
      <td class="domain">macrostructure, linkage</td>
      <td class="term">Unlinked</td>
      <td>Adjacent microbialite forms remain separate without physical connection.</td>
      <td>Grey and Awramik (2020); p. 63; fig. 46</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroplanview" data-status="provisional">
      <td class="domain">macrostructure, plan view</td>
      <td class="term">Crescentic</td>
      <td>Curved into a crescent or arc shape.</td>
      <td>Grey and Awramik (2020); p. 55; fig. 38</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroplanview" data-status="provisional">
      <td class="domain">macrostructure, plan view</td>
      <td class="term">Lobate 1</td>
      <td>Margins divided into broad rounded lobes.</td>
      <td>Grey and Awramik (2020); p. 55; fig. 38</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroplanview" data-status="provisional">
      <td class="domain">macrostructure, plan view</td>
      <td class="term">Lobate 2</td>
      <td>Margins divided into more pronounced or irregular lobes.</td>
      <td>Grey and Awramik (2020); p. 55; fig. 38</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroplanview" data-status="provisional">
      <td class="domain">macrostructure, plan view</td>
      <td class="term">Lobate 3</td>
      <td>Margins strongly subdivided into multiple distinct lobes.</td>
      <td>Grey and Awramik (2020); p. 55; fig. 38</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroplanview" data-status="provisional">
      <td class="domain">macrostructure, plan view</td>
      <td class="term">Circular</td>
      <td>Circular in plan view with approximately equal dimensions in all directions.</td>
      <td>Grey and Awramik (2020); p. 55; fig. 38</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroplanview" data-status="provisional">
      <td class="domain">macrostructure, plan view</td>
      <td class="term">Ovate</td>
      <td>Oval to egg-shaped in plan view with one axis longer than the other.</td>
      <td>Grey and Awramik (2020); p. 55; fig. 38</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroplanview" data-status="provisional">
      <td class="domain">macrostructure, plan view</td>
      <td class="term">Lanceolate</td>
      <td>Broadly lance-shaped with tapering ends.</td>
      <td>Grey and Awramik (2020); p. 55; fig. 38</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroplanview" data-status="provisional">
      <td class="domain">macrostructure, plan view</td>
      <td class="term">Linear</td>
      <td>Strongly elongated in one direction relative to width.</td>
      <td>Grey and Awramik (2020); p. 55; fig. 38</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroplanview" data-status="provisional">
      <td class="domain">macrostructure, plan view</td>
      <td class="term">Pitted</td>
      <td>Surface contains depressions or pit-like indentations.</td>
      <td>Grey and Awramik (2020); p. 55; fig. 38</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroplanview" data-status="provisional">
      <td class="domain">macrostructure, plan view</td>
      <td class="term">Labyrinthine</td>
      <td>Irregularly winding or maze-like in plan view.</td>
      <td>Grey and Awramik (2020); p. 55; fig. 38</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroplanview" data-status="provisional">
      <td class="domain">macrostructure, plan view</td>
      <td class="term">Polygonal</td>
      <td>Composed of multiple angular sides forming polygonal outlines.</td>
      <td>Grey and Awramik (2020); p. 55; fig. 38</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroplanview" data-status="provisional">
      <td class="domain">macrostructure, plan view</td>
      <td class="term">Scutate</td>
      <td>Shield-shaped in plan view with rounded and tapering margins.</td>
      <td>Grey and Awramik (2020); p. 55; fig. 38</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroshape" data-status="provisional">
      <td class="domain">macrostructure, shape</td>
      <td class="term">Oncoid</td>
      <td>an unattached stromatolite</td>
      <td>Grey and Awramik (2020); p. 63; fig. 51</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroshape" data-status="provisional">
      <td class="domain">macrostructure, shape</td>
      <td class="term">Plumose</td>
      <td>a microbialite with an apparent
central stem (support) and many fine branches that bifurcate and coalesce, producing an overall feathery appearance</td>
      <td>Grey and Awramik (2020); p. 63; fig. 51</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroshape" data-status="provisional">
      <td class="domain">macrostructure, shape</td>
      <td class="term">Layered</td>
      <td>a microbialite that shows little or no positive relief. Laminae, where present, are parallel, nearly planar and continuous.</td>
      <td>Grey and Awramik (2020); p. 61; fig. 51</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroshape" data-status="provisional">
      <td class="domain">macrostructure, shape</td>
      <td class="term">Domical</td>
      <td>an individual microbialite that arises directly from the substrate, and has a convex vault</td>
      <td>Grey and Awramik (2020); p. 61; fig. 51</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroshape" data-status="provisional">
      <td class="domain">macrostructure, shape</td>
      <td class="term">Columnar</td>
      <td>a nonbranching microbialite in which height is much greater than the width.</td>
      <td>Grey and Awramik (2020); p. 61; fig. 51</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroshape" data-status="provisional">
      <td class="domain">macrostructure, shape</td>
      <td class="term">Conical</td>
      <td>a non-branching
microbialite that commonly has a circular to oval (more rarely polygonal) base, and which tapers to a point</td>
      <td>Grey and Awramik (2020); p. 61; fig. 51</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroshape" data-status="provisional">
      <td class="domain">macrostructure, shape</td>
      <td class="term">Branched</td>
      <td>any microbialite that exhibits branching can be referred to as a branched microbialite.</td>
      <td>Grey and Awramik (2020); p. 61; fig. 51</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroshape" data-status="provisional">
      <td class="domain">macrostructure, shape</td>
      <td class="term">Compound</td>
      <td>microbialites that have more than one type of coexisting organization within the same type of microbialite</td>
      <td>Grey and Awramik (2020); p. 63; fig. 51</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroshape" data-status="provisional">
      <td class="domain">macrostructure, shape</td>
      <td class="term">Macerate</td>
      <td>3D shape of a microbialite that resembles labyrinthine, hedge-like mazes in plan view and has a cerebroid surface view</td>
      <td>Grey and Awramik (2020); p. 63; fig. 51</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacroshape" data-status="provisional">
      <td class="domain">macrostructure, shape</td>
      <td class="term">Pitted</td>
      <td>a microbialite with
numerous, relatively deep, steep-sided depressions extending into the microbialite and filled with sediment</td>
      <td>Grey and Awramik (2020); p. 63; fig. 51</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrospacing" data-status="provisional">
      <td class="domain">macrostructure, spacing</td>
      <td class="term">Contiguous</td>
      <td>Adjacent microbialite forms are in direct contact with little or no separation.</td>
      <td>Grey and Awramik (2020); p. 63; fig. 47</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrospacing" data-status="provisional">
      <td class="domain">macrostructure, spacing</td>
      <td class="term">Closely spaced</td>
      <td>Microbialite forms are separated by narrow intervening spaces.</td>
      <td>Grey and Awramik (2020); p. 63; fig. 47</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrospacing" data-status="provisional">
      <td class="domain">macrostructure, spacing</td>
      <td class="term">Openly spaced</td>
      <td>Microbialite forms are separated by broad open spaces.</td>
      <td>Grey and Awramik (2020); p. 63; fig. 47</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmacrospacing" data-status="provisional">
      <td class="domain">macrostructure, spacing</td>
      <td class="term">Isolated</td>
      <td>Individual microbialite forms remain distinctly separated from neighboring forms.</td>
      <td>Grey and Awramik (2020); p. 63; fig. 47</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegabedgeometry" data-status="provisional">
      <td class="domain">megastructure, bed geometry</td>
      <td class="term">Tabular</td>
      <td>Laterally extensive bed with relatively uniform thickness.</td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegabedgeometry" data-status="provisional">
      <td class="domain">megastructure, bed geometry</td>
      <td class="term">Lenticular</td>
      <td>Lens-shaped bed that thickens toward the center and thins toward the margins.</td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegabedgeometry" data-status="provisional">
      <td class="domain">megastructure, bed geometry</td>
      <td class="term">Wedge-shaped</td>
      <td>Bed geometry that systematically thickens in one direction to form a wedge.</td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegabedgeometry" data-status="provisional">
      <td class="domain">megastructure, bed geometry</td>
      <td class="term">Concave-up</td>
      <td>Bed with an upward-curving basal contact geometry in cross section.</td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegabedgeometry" data-status="provisional">
      <td class="domain">megastructure, bed geometry</td>
      <td class="term">Concave-down</td>
      <td>Bed with a downward-curving upper contact geometry in cross section.</td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegabuildupinterface" data-status="provisional">
      <td class="domain">megastructure, buildup interface</td>
      <td class="term">Discrete</td>
      <td>Boundary between adjacent buildups remains clearly separated and well defined.</td>
      <td>Grey and Awramik (2020); p. 16; fig. 10</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegabuildupinterface" data-status="provisional">
      <td class="domain">megastructure, buildup interface</td>
      <td class="term">intertonguing</td>
      <td>Adjacent buildups merge through interpenetrating or interlocking margins.</td>
      <td>Grey and Awramik (2020); p. 16; fig. 10</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegabuilduptype" data-status="provisional">
      <td class="domain">megastructure, buildup type</td>
      <td class="term">Bioherm</td>
      <td>Localized mound-like microbialite buildup with positive relief above the surrounding surface.</td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegabuilduptype" data-status="provisional">
      <td class="domain">megastructure, buildup type</td>
      <td class="term">Biostrome</td>
      <td>Laterally extensive sheet-like microbialite buildup with relatively low relief.</td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegabuilduptype" data-status="provisional">
      <td class="domain">megastructure, buildup type</td>
      <td class="term">isolated head</td>
      <td>Single detached microbialite head surrounded by sediment or open space.</td>
      <td>Database operational terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegabuilduptype" data-status="provisional">
      <td class="domain">megastructure, buildup type</td>
      <td class="term">Depression</td>
      <td>Negative-relief area or hollow with preserved microbialite textures.</td>
      <td>Database operational terminology</td>
      <td>provisional</td>
      <td>This is something we see that probably results from the erosion of a stromatolitic bioherm, leaving the basal stromatolitic textures visible as a sub-circular depression.</td>
    </tr>
    <tr data-domain="tlkpmegabuilduptype" data-status="provisional">
      <td class="domain">megastructure, buildup type</td>
      <td class="term">Float</td>
      <td>Detached or transported microbialite mass not in outcrop or rock body.</td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegadepositionalsetting" data-status="provisional">
      <td class="domain">megastructure, depositional setting</td>
      <td class="term">Back-reef</td>
      <td>Protected marine environment landward of a reef structure.</td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegadepositionalsetting" data-status="provisional">
      <td class="domain">megastructure, depositional setting</td>
      <td class="term">Non-Marine</td>
      <td>Depositional setting not directly influenced by marine conditions.</td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegadepositionalsetting" data-status="provisional">
      <td class="domain">megastructure, depositional setting</td>
      <td class="term">Lacustrine</td>
      <td>Depositional environment associated with lakes.</td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegadepositionalsetting" data-status="provisional">
      <td class="domain">megastructure, depositional setting</td>
      <td class="term">Fluvial</td>
      <td>Depositional environment associated with river or stream systems.</td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegadepositionalsetting" data-status="provisional">
      <td class="domain">megastructure, depositional setting</td>
      <td class="term">Evaporitic</td>
      <td>Environment dominated by evaporite mineral precipitation due to high evaporation.</td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegadepositionalsetting" data-status="provisional">
      <td class="domain">megastructure, depositional setting</td>
      <td class="term">Eolian</td>
      <td>Wind-dominated depositional environment.</td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegadepositionalsetting" data-status="provisional">
      <td class="domain">megastructure, depositional setting</td>
      <td class="term">Spring</td>
      <td>Depositional environment associated with groundwater discharge or hydrothermal springs.</td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegadepositionalsetting" data-status="provisional">
      <td class="domain">megastructure, depositional setting</td>
      <td class="term">Marine</td>
      <td>Depositional setting associated with seawater environments.</td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegadepositionalsetting" data-status="provisional">
      <td class="domain">megastructure, depositional setting</td>
      <td class="term">Sub-tidal</td>
      <td>Permanently submerged shallow marine environment below low tide level.</td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegadepositionalsetting" data-status="provisional">
      <td class="domain">megastructure, depositional setting</td>
      <td class="term">inter-tidal</td>
      <td>Environment alternately exposed and submerged by tidal fluctuations.</td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegadepositionalsetting" data-status="provisional">
      <td class="domain">megastructure, depositional setting</td>
      <td class="term">Supra-tidal</td>
      <td>Environment above normal high tide level with only occasional marine inundation.</td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegadepositionalsetting" data-status="provisional">
      <td class="domain">megastructure, depositional setting</td>
      <td class="term">Beach</td>
      <td>Wave-influenced shoreline composed predominantly of sediment.</td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegadepositionalsetting" data-status="provisional">
      <td class="domain">megastructure, depositional setting</td>
      <td class="term">Shelf</td>
      <td>Broad shallow marine platform extending from shore to deeper water.</td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegadepositionalsetting" data-status="provisional">
      <td class="domain">megastructure, depositional setting</td>
      <td class="term">Slope</td>
      <td>Inclined marine surface descending from shelf into deeper basin environments.</td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegadepositionalsetting" data-status="provisional">
      <td class="domain">megastructure, depositional setting</td>
      <td class="term">Reef</td>
      <td>Wave-resistant biologically constructed carbonate buildup.</td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegahorizontalscale" data-status="provisional">
      <td class="domain">megastructure, horizontal scale</td>
      <td class="term">&lt;5 cm</td>
      <td><em>Definition pending</em></td>
      <td></td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegahorizontalscale" data-status="provisional">
      <td class="domain">megastructure, horizontal scale</td>
      <td class="term">5-10 cm</td>
      <td><em>Definition pending</em></td>
      <td></td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegahorizontalscale" data-status="provisional">
      <td class="domain">megastructure, horizontal scale</td>
      <td class="term">10-20 cm</td>
      <td><em>Definition pending</em></td>
      <td></td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegahorizontalscale" data-status="provisional">
      <td class="domain">megastructure, horizontal scale</td>
      <td class="term">20-50 cm</td>
      <td><em>Definition pending</em></td>
      <td></td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegahorizontalscale" data-status="provisional">
      <td class="domain">megastructure, horizontal scale</td>
      <td class="term">50--100 cm</td>
      <td><em>Definition pending</em></td>
      <td></td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegahorizontalscale" data-status="provisional">
      <td class="domain">megastructure, horizontal scale</td>
      <td class="term">1-2 m</td>
      <td><em>Definition pending</em></td>
      <td></td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegahorizontalscale" data-status="provisional">
      <td class="domain">megastructure, horizontal scale</td>
      <td class="term">2-10 m</td>
      <td><em>Definition pending</em></td>
      <td></td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegahorizontalscale" data-status="provisional">
      <td class="domain">megastructure, horizontal scale</td>
      <td class="term">&gt;10 m</td>
      <td><em>Definition pending</em></td>
      <td></td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegainitiation" data-status="provisional">
      <td class="domain">megastructure, initiation</td>
      <td class="term">On substrate</td>
      <td>Microbialite growth begins directly on the underlying substrate surface.</td>
      <td>Grey and Awramik (2020); p. 45; fig. 30</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegainitiation" data-status="provisional">
      <td class="domain">megastructure, initiation</td>
      <td class="term">On stratiform stromatolite</td>
      <td>Microbialite growth initiates on an existing stratiform stromatolite surface.</td>
      <td>Grey and Awramik (2020); p. 45; fig. 30</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegainitiation" data-status="provisional">
      <td class="domain">megastructure, initiation</td>
      <td class="term">On domical stromatolite</td>
      <td>Microbialite growth initiates on an existing domical stromatolite surface.</td>
      <td>Grey and Awramik (2020); p. 45; fig. 30</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegainitiation" data-status="provisional">
      <td class="domain">megastructure, initiation</td>
      <td class="term">On other microbialite</td>
      <td>Microbialite growth initiates on a pre-existing microbialite structure of another form.</td>
      <td>Grey and Awramik (2020); p. 45; fig. 30</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegalat_long_quality" data-status="provisional">
      <td class="domain">megastructure, latitude/longitude quality</td>
      <td class="term">Very high (GPS location from field)</td>
      <td>Coordinates obtained directly from GPS measurements or embedded geolocation metadata with minimal positional uncertainty</td>
      <td>Database operational terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegalat_long_quality" data-status="provisional">
      <td class="domain">megastructure, latitude/longitude quality</td>
      <td class="term">High (Located precisely using GIS)</td>
      <td>Coordinates determined precisely using maps, GIS data, or clearly documented locality descriptions</td>
      <td>Database operational terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegalat_long_quality" data-status="provisional">
      <td class="domain">megastructure, latitude/longitude quality</td>
      <td class="term">Medium (Located based on high quality map)</td>
      <td>Coordinates estimated from generalized locality information or regional geographic context</td>
      <td>Database operational terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegalat_long_quality" data-status="provisional">
      <td class="domain">megastructure, latitude/longitude quality</td>
      <td class="term">Low (Estimated from map)</td>
      <td>Coordinates approximated from coarse-scale maps or incomplete locality descriptions</td>
      <td>Database operational terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegalat_long_quality" data-status="provisional">
      <td class="domain">megastructure, latitude/longitude quality</td>
      <td class="term">Very Low (Estimated from description or very small scale map)</td>
      <td>Coordinates inferred from vague descriptive information with substantial positional uncertainty</td>
      <td>Database operational terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegalithology" data-status="provisional">
      <td class="domain">megastructure, lithology</td>
      <td class="term">Limestone</td>
      <td><em>Definition pending</em></td>
      <td></td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegalithology" data-status="provisional">
      <td class="domain">megastructure, lithology</td>
      <td class="term">Dolostone</td>
      <td><em>Definition pending</em></td>
      <td></td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegalithology" data-status="provisional">
      <td class="domain">megastructure, lithology</td>
      <td class="term">Gypsum</td>
      <td><em>Definition pending</em></td>
      <td></td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegalithology" data-status="provisional">
      <td class="domain">megastructure, lithology</td>
      <td class="term">Chert</td>
      <td><em>Definition pending</em></td>
      <td></td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegalithology" data-status="provisional">
      <td class="domain">megastructure, lithology</td>
      <td class="term">Sandstone</td>
      <td><em>Definition pending</em></td>
      <td></td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegamegastructureshape" data-status="provisional">
      <td class="domain">megastructure, megastructure shape</td>
      <td class="term">Pedestal</td>
      <td>Buildup elevated on a narrower supporting base or stem.</td>
      <td>Grey and Awramik (2020); p. 16; fig. 10</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegamegastructureshape" data-status="provisional">
      <td class="domain">megastructure, megastructure shape</td>
      <td class="term">Tabular</td>
      <td>Laterally extensive buildup with relatively flat upper and lower surfaces.</td>
      <td>Grey and Awramik (2020); p. 16; fig. 10</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegamegastructureshape" data-status="provisional">
      <td class="domain">megastructure, megastructure shape</td>
      <td class="term">Domical</td>
      <td>Rounded mound-like buildup with positive relief.</td>
      <td>Grey and Awramik (2020); p. 16; fig. 10</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegamegastructureshape" data-status="provisional">
      <td class="domain">megastructure, megastructure shape</td>
      <td class="term">Subspherical</td>
      <td>Broadly rounded buildup approaching spherical geometry.</td>
      <td>Grey and Awramik (2020); p. 16; fig. 10</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegamegastructureshape" data-status="provisional">
      <td class="domain">megastructure, megastructure shape</td>
      <td class="term">Tabular-undulating</td>
      <td>Tabular buildup with gently undulating upper morphology.</td>
      <td>Grey and Awramik (2020); p. 16; fig. 10</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegamegastructureshape" data-status="provisional">
      <td class="domain">megastructure, megastructure shape</td>
      <td class="term">Nodular</td>
      <td>Buildup composed of rounded nodular masses.</td>
      <td>Grey and Awramik (2020); p. 16; fig. 10</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegamegastructureshape" data-status="provisional">
      <td class="domain">megastructure, megastructure shape</td>
      <td class="term">Club-shaped</td>
      <td>Buildup widened upward relative to its base.</td>
      <td>Grey and Awramik (2020); p. 16; fig. 10</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegamegastructureshape" data-status="provisional">
      <td class="domain">megastructure, megastructure shape</td>
      <td class="term">Egg-shaped</td>
      <td>Buildup narrowed at one end and broader at the other, resembling an egg shape.</td>
      <td>Grey and Awramik (2020); p. 16; fig. 10</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegamegastructureshape" data-status="provisional">
      <td class="domain">megastructure, megastructure shape</td>
      <td class="term">Ellipsoidal</td>
      <td>Buildup with elongated rounded geometry in three dimensions.</td>
      <td>Grey and Awramik (2020); p. 16; fig. 10</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegamicrobialitetypes" data-status="provisional">
      <td class="domain">megastructure, microbialite types</td>
      <td class="term">Stromatolite</td>
      <td>Laminated microbialite produced through microbial trapping, binding, and/or mineral precipitation.</td>
      <td>Grey and Awramik (2020); p. 27; fig. 1</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegamicrobialitetypes" data-status="provisional">
      <td class="domain">megastructure, microbialite types</td>
      <td class="term">Thrombolite</td>
      <td>Microbialite characterized by a clotted mesostructure rather than distinct lamination.</td>
      <td>Grey and Awramik (2020); p. 27; fig. 1</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegamicrobialitetypes" data-status="provisional">
      <td class="domain">megastructure, microbialite types</td>
      <td class="term">Dendrolite</td>
      <td>Non-laminated microbialite composed of branching shrub-like structures.</td>
      <td>Grey and Awramik (2020); p. 27; fig. 1</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegamicrobialitetypes" data-status="provisional">
      <td class="domain">megastructure, microbialite types</td>
      <td class="term">Leiolite</td>
      <td>Structureless or weakly structured microbialite lacking obvious lamination, clots, or dendritic fabrics.</td>
      <td>Grey and Awramik (2020); p. 27; fig. 1</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegamicrobialitetypes" data-status="provisional">
      <td class="domain">megastructure, microbialite types</td>
      <td class="term">MISS</td>
      <td>Sedimentary structures formed or modified through microbial activity and microbial mat interactions with sediment.</td>
      <td>Grey and Awramik (2020); p. 27; fig. 1</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegamicrobialitetypes" data-status="provisional">
      <td class="domain">megastructure, microbialite types</td>
      <td class="term">Conical void</td>
      <td>Conical depression with erosional contacts, typically lined by thin bed.</td>
      <td>Hickson; p. 27; fig. 1</td>
      <td>provisional</td>
      <td>These are features that may be related to spring sources but may have microbialitic textures associated with them.</td>
    </tr>
    <tr data-domain="tlkpmegamicrobialitetypes" data-status="provisional">
      <td class="domain">megastructure, microbialite types</td>
      <td class="term">Oncolite</td>
      <td>Coated carbonate grain formed by concentric or irregular microbial accretion around a mobile nucleus.</td>
      <td>Hickson; p. 27; fig. 1</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegasedinterface" data-status="provisional">
      <td class="domain">megastructure, sediment interface</td>
      <td class="term">Interbiohermal space</td>
      <td>Area between adjacent bioherms within a microbialite buildup</td>
      <td>Grey and Awramik (2020); p. 54; fig. 11</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegasedinterface" data-status="provisional">
      <td class="domain">megastructure, sediment interface</td>
      <td class="term">Interspace</td>
      <td>Area between adjacent microbialite structures such as heads, domes, columns, cones, branches, or oncoids</td>
      <td>Grey and Awramik (2020); p. 54; fig. 11</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegasedinterface" data-status="provisional">
      <td class="domain">megastructure, sediment interface</td>
      <td class="term">Interfascicular space</td>
      <td>Area between adjacent fascicles or branches within a branched microbialite structure</td>
      <td>Grey and Awramik (2020); p. 54; fig. 11</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegasubstrate" data-status="provisional">
      <td class="domain">megastructure, substrate</td>
      <td class="term">Older Microbialite</td>
      <td>Microbialite growing on an older lithified microbialite surface</td>
      <td>Grey and Awramik (2020); p. 39; fig. 24</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegasubstrate" data-status="provisional">
      <td class="domain">megastructure, substrate</td>
      <td class="term">Encrusting</td>
      <td>Microbialite coating or lining a fracture, cavity, or other hard substrate surface</td>
      <td>Grey and Awramik (2020); p. 39; fig. 24</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegasubstrate" data-status="provisional">
      <td class="domain">megastructure, substrate</td>
      <td class="term">Clast-Supported</td>
      <td>Microbialite growing on or around clasts that form the substrate</td>
      <td>Grey and Awramik (2020); p. 39; fig. 24</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegaverticalscale" data-status="provisional">
      <td class="domain">megastructure, vertical scale</td>
      <td class="term">&lt;5 cm</td>
      <td><em>Definition pending</em></td>
      <td></td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegaverticalscale" data-status="provisional">
      <td class="domain">megastructure, vertical scale</td>
      <td class="term">5-10 cm</td>
      <td><em>Definition pending</em></td>
      <td></td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegaverticalscale" data-status="provisional">
      <td class="domain">megastructure, vertical scale</td>
      <td class="term">10-20 cm</td>
      <td><em>Definition pending</em></td>
      <td></td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegaverticalscale" data-status="provisional">
      <td class="domain">megastructure, vertical scale</td>
      <td class="term">20-50 cm</td>
      <td><em>Definition pending</em></td>
      <td></td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegaverticalscale" data-status="provisional">
      <td class="domain">megastructure, vertical scale</td>
      <td class="term">50--100 cm</td>
      <td><em>Definition pending</em></td>
      <td></td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegaverticalscale" data-status="provisional">
      <td class="domain">megastructure, vertical scale</td>
      <td class="term">1-2 m</td>
      <td><em>Definition pending</em></td>
      <td></td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegaverticalscale" data-status="provisional">
      <td class="domain">megastructure, vertical scale</td>
      <td class="term">2-10 m</td>
      <td><em>Definition pending</em></td>
      <td></td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmegaverticalscale" data-status="provisional">
      <td class="domain">megastructure, vertical scale</td>
      <td class="term">&gt;10 m</td>
      <td><em>Definition pending</em></td>
      <td></td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesoalternation" data-status="provisional">
      <td class="domain">mesostructure, alternation</td>
      <td class="term">Even</td>
      <td>Adjacent laminae composed of similar microstructural types with distinct sharp boundaries</td>
      <td>Grey and Awramik (2020); p. 124; fig. 116</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesoalternation" data-status="provisional">
      <td class="domain">mesostructure, alternation</td>
      <td class="term">Composite</td>
      <td>Adjacent laminae composed of different microstructural types with both sharp and gradational boundaries</td>
      <td>Grey and Awramik (2020); p. 124; fig. 116</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesoalternation" data-status="provisional">
      <td class="domain">mesostructure, alternation</td>
      <td class="term">Gradational</td>
      <td>Light and dark laminae that grade gradually into one another without sharp boundaries</td>
      <td>Grey and Awramik (2020); p. 124; fig. 116</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesoalternation" data-status="provisional">
      <td class="domain">mesostructure, alternation</td>
      <td class="term">Film bounded smooth</td>
      <td>Adjacent laminae separated by a smooth thin film, commonly finer grained than adjacent laminae</td>
      <td>Grey and Awramik (2020); p. 124; fig. 116</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesoalternation" data-status="provisional">
      <td class="domain">mesostructure, alternation</td>
      <td class="term">Film bounded wavy</td>
      <td>Adjacent laminae separated by a wavy or undulose thin film</td>
      <td>Grey and Awramik (2020); p. 124; fig. 116</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesoalternation" data-status="provisional">
      <td class="domain">mesostructure, alternation</td>
      <td class="term">Intercalated sed_cement</td>
      <td>Laminae containing fenestrae later infilled by sediment or cement</td>
      <td>Grey and Awramik (2020); p. 124; fig. 116</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesoalternation" data-status="provisional">
      <td class="domain">mesostructure, alternation</td>
      <td class="term">Intercalated recrystallized</td>
      <td>Laminae separated or displaced by later infilling of fenestrae or voids</td>
      <td>Grey and Awramik (2020); p. 124; fig. 116</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesoarchitecture" data-status="provisional">
      <td class="domain">mesostructure, architecture</td>
      <td class="term">Banded</td>
      <td>Laminae organized into broad laterally continuous bands with consistent texture or microstructure</td>
      <td>Grey and Awramik (2020); p. 157; fig. 150</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesoarchitecture" data-status="provisional">
      <td class="domain">mesostructure, architecture</td>
      <td class="term">Filmy</td>
      <td>Laminae composed of thin film-like layers commonly associated with film-bounded alternation</td>
      <td>Grey and Awramik (2020); p. 157; fig. 150</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesoarchitecture" data-status="provisional">
      <td class="domain">mesostructure, architecture</td>
      <td class="term">Striated</td>
      <td>Laminae displaying fine parallel linear markings or streaks</td>
      <td>Grey and Awramik (2020); p. 157; fig. 150</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesoarchitecture" data-status="provisional">
      <td class="domain">mesostructure, architecture</td>
      <td class="term">Streaky</td>
      <td>Laminae composed of discontinuous irregular ribbon-like streaks</td>
      <td>Grey and Awramik (2020); p. 157; fig. 150</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesoarchitecture" data-status="provisional">
      <td class="domain">mesostructure, architecture</td>
      <td class="term">Tussocky</td>
      <td>Laminae forming uneven tufted or hummocky surface patterns</td>
      <td>Grey and Awramik (2020); p. 157; fig. 150</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesoarchitecture" data-status="provisional">
      <td class="domain">mesostructure, architecture</td>
      <td class="term">Pillared</td>
      <td>Laminae organized into vertical pillar-like structures</td>
      <td>Grey and Awramik (2020); p. 157; fig. 150</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesoarchitecture" data-status="provisional">
      <td class="domain">mesostructure, architecture</td>
      <td class="term">Vermiform</td>
      <td>Laminae forming worm-like irregular tubular patterns</td>
      <td>Grey and Awramik (2020); p. 157; fig. 150</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesoarchitecture" data-status="provisional">
      <td class="domain">mesostructure, architecture</td>
      <td class="term">Alveolar</td>
      <td>Laminae containing interconnected cavity-like or honeycomb structures</td>
      <td>Grey and Awramik (2020); p. 157; fig. 150</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesoclothierarchy" data-status="provisional">
      <td class="domain">mesostructure, clot hierarchy</td>
      <td class="term">Miniclots</td>
      <td>Small individual clots that form the basic component of thrombolitic fabric</td>
      <td>Grey and Awramik (2020); p. 166; fig. 157</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesoclothierarchy" data-status="provisional">
      <td class="domain">mesostructure, clot hierarchy</td>
      <td class="term">Mesoclots</td>
      <td>Intermediate-sized aggregates composed of grouped miniclots</td>
      <td>Grey and Awramik (2020); p. 166; fig. 157</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesoclothierarchy" data-status="provisional">
      <td class="domain">mesostructure, clot hierarchy</td>
      <td class="term">Maxiclots</td>
      <td>Large composite clot structures composed of multiple mesoclots or clot aggregates</td>
      <td>Grey and Awramik (2020); p. 166; fig. 157</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesoclotshape" data-status="provisional">
      <td class="domain">mesostructure, clot shape</td>
      <td class="term">Saccate</td>
      <td>Clots shaped like sacs or pouch-like bodies</td>
      <td>Grey and Awramik (2020); p. 171; fig. 161</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesoclotshape" data-status="provisional">
      <td class="domain">mesostructure, clot shape</td>
      <td class="term">Arborescent</td>
      <td>Clots displaying tree-like branching morphology</td>
      <td>Grey and Awramik (2020); p. 171; fig. 161</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesoclotshape" data-status="provisional">
      <td class="domain">mesostructure, clot shape</td>
      <td class="term">Diffuse</td>
      <td>Clots lacking distinct boundaries or definite shape</td>
      <td>Grey and Awramik (2020); p. 171; fig. 161</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesoclotshape" data-status="provisional">
      <td class="domain">mesostructure, clot shape</td>
      <td class="term">Rounded</td>
      <td>Clots with nearly circular outlines</td>
      <td>Grey and Awramik (2020); p. 171; fig. 161</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesoclotshape" data-status="provisional">
      <td class="domain">mesostructure, clot shape</td>
      <td class="term">Subrounded</td>
      <td>Clots with rounded but somewhat irregular outlines</td>
      <td>Grey and Awramik (2020); p. 171; fig. 161</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesoclotshape" data-status="provisional">
      <td class="domain">mesostructure, clot shape</td>
      <td class="term">Oblong</td>
      <td>Clots elongated in one direction with rounded ends</td>
      <td>Grey and Awramik (2020); p. 171; fig. 161</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesoclotshape" data-status="provisional">
      <td class="domain">mesostructure, clot shape</td>
      <td class="term">Lanceolate</td>
      <td>Clots elongated and tapering toward one or both ends</td>
      <td>Grey and Awramik (2020); p. 171; fig. 161</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesoclotshape" data-status="provisional">
      <td class="domain">mesostructure, clot shape</td>
      <td class="term">Crescentic</td>
      <td>Clots curved into crescent-like forms</td>
      <td>Grey and Awramik (2020); p. 171; fig. 161</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesoclotshape" data-status="provisional">
      <td class="domain">mesostructure, clot shape</td>
      <td class="term">Scutate</td>
      <td>Clots shaped like small shields or flattened rounded polygons</td>
      <td>Grey and Awramik (2020); p. 171; fig. 161</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesoclotshape" data-status="provisional">
      <td class="domain">mesostructure, clot shape</td>
      <td class="term">Pendant</td>
      <td>Clots hanging downward from overlying structures</td>
      <td>Grey and Awramik (2020); p. 171; fig. 161</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesoclotshape" data-status="provisional">
      <td class="domain">mesostructure, clot shape</td>
      <td class="term">Lobate</td>
      <td>Clots with irregular lobed margins</td>
      <td>Grey and Awramik (2020); p. 171; fig. 161</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesograintypes" data-status="provisional">
      <td class="domain">mesostructure, grain types</td>
      <td class="term">Peloidal</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesograintypes" data-status="provisional">
      <td class="domain">mesostructure, grain types</td>
      <td class="term">Aphanitic</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesograintypes" data-status="provisional">
      <td class="domain">mesostructure, grain types</td>
      <td class="term">Oolitic</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesograintypes" data-status="provisional">
      <td class="domain">mesostructure, grain types</td>
      <td class="term">Pisoids</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesograintypes" data-status="provisional">
      <td class="domain">mesostructure, grain types</td>
      <td class="term">Oncoids</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesolaminainheritance" data-status="provisional">
      <td class="domain">mesostructure, lamina inheritance</td>
      <td class="term">Low</td>
      <td>Successive laminae show little resemblance to preceding laminae and inherit few underlying features</td>
      <td>Grey and Awramik (2020); p. 139; fig. 130</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesolaminainheritance" data-status="provisional">
      <td class="domain">mesostructure, lamina inheritance</td>
      <td class="term">Medium</td>
      <td>Successive laminae inherit some features and morphology from preceding laminae</td>
      <td>Grey and Awramik (2020); p. 139; fig. 130</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesolaminainheritance" data-status="provisional">
      <td class="domain">mesostructure, lamina inheritance</td>
      <td class="term">High</td>
      <td>Successive laminae strongly replicate the morphology and features of preceding laminae</td>
      <td>Grey and Awramik (2020); p. 139; fig. 130</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesolaminainheritance" data-status="provisional">
      <td class="domain">mesostructure, lamina inheritance</td>
      <td class="term">Variable</td>
      <td>Degree of inheritance changes within the microbialite or between successive laminae</td>
      <td>Grey and Awramik (2020); p. 139; fig. 130</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesolampattern" data-status="provisional">
      <td class="domain">mesostructure, lamina pattern</td>
      <td class="term">Couplet</td>
      <td>Laminae composed of repeating paired light and dark layers</td>
      <td>Grey and Awramik (2020); p. 120; fig. 106</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesolampattern" data-status="provisional">
      <td class="domain">mesostructure, lamina pattern</td>
      <td class="term">Non-couplet</td>
      <td>Laminae lacking consistent paired light and dark layering</td>
      <td>Grey and Awramik (2020); p. 120; fig. 106</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesolampattern" data-status="provisional">
      <td class="domain">mesostructure, lamina pattern</td>
      <td class="term">Variable mostly couplet</td>
      <td>Lamination dominated by couplets but containing some non-couplet intervals</td>
      <td>Grey and Awramik (2020); p. 120; fig. 106</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesolampattern" data-status="provisional">
      <td class="domain">mesostructure, lamina pattern</td>
      <td class="term">Variable mostly non couplet</td>
      <td>Lamination dominated by non-couplet intervals but containing some couplets</td>
      <td>Grey and Awramik (2020); p. 120; fig. 106</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesolampattern" data-status="provisional">
      <td class="domain">mesostructure, lamina pattern</td>
      <td class="term">Variable</td>
      <td>Lamination pattern changes irregularly between couplet and non-couplet organization</td>
      <td>Grey and Awramik (2020); p. 120; fig. 106</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesolamprofile" data-status="provisional">
      <td class="domain">mesostructure, lamina profile</td>
      <td class="term">Conical</td>
      <td>Laminae tapering upward toward a pointed apex</td>
      <td>Grey and Awramik (2020); p. 133; fig. 120</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesolamprofile" data-status="provisional">
      <td class="domain">mesostructure, lamina profile</td>
      <td class="term">Angulate</td>
      <td>Laminae composed of sharply angled segments or bends</td>
      <td>Grey and Awramik (2020); p. 133; fig. 120</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesolamprofile" data-status="provisional">
      <td class="domain">mesostructure, lamina profile</td>
      <td class="term">Plenicinct</td>
      <td>Laminae forming fully concentric curved bands enclosing the structure</td>
      <td>Grey and Awramik (2020); p. 133; fig. 120</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesolamprofile" data-status="provisional">
      <td class="domain">mesostructure, lamina profile</td>
      <td class="term">Concave</td>
      <td>Laminae curved downward in profile</td>
      <td>Grey and Awramik (2020); p. 133; fig. 120</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesolamprofile" data-status="provisional">
      <td class="domain">mesostructure, lamina profile</td>
      <td class="term">Flat</td>
      <td>Laminae with little or no curvature</td>
      <td>Grey and Awramik (2020); p. 133; fig. 120</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesolamprofile" data-status="provisional">
      <td class="domain">mesostructure, lamina profile</td>
      <td class="term">Gently convex</td>
      <td>Laminae with broad low upward convexity</td>
      <td>Grey and Awramik (2020); p. 133; fig. 120</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesolamprofile" data-status="provisional">
      <td class="domain">mesostructure, lamina profile</td>
      <td class="term">Steeply convex</td>
      <td>Laminae with strong upward convexity and high relief</td>
      <td>Grey and Awramik (2020); p. 133; fig. 120</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesolamprofile" data-status="provisional">
      <td class="domain">mesostructure, lamina profile</td>
      <td class="term">Parabolic</td>
      <td>Laminae with smoothly curved upward profiles approximating a parabola</td>
      <td>Grey and Awramik (2020); p. 133; fig. 120</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesolamprofile" data-status="provisional">
      <td class="domain">mesostructure, lamina profile</td>
      <td class="term">Penecinct</td>
      <td>Laminae forming nearly complete concentric curved bands</td>
      <td>Grey and Awramik (2020); p. 133; fig. 120</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesolamprofile" data-status="provisional">
      <td class="domain">mesostructure, lamina profile</td>
      <td class="term">Rectangular</td>
      <td>Laminae with flat tops and steep sides forming box-like profiles</td>
      <td>Grey and Awramik (2020); p. 133; fig. 120</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesolamprofile" data-status="provisional">
      <td class="domain">mesostructure, lamina profile</td>
      <td class="term">Rhombic</td>
      <td>Laminae with diamond-shaped or angled profiles</td>
      <td>Grey and Awramik (2020); p. 133; fig. 120</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesolamwaviness" data-status="provisional">
      <td class="domain">mesostructure, lamina waviness</td>
      <td class="term">Straight</td>
      <td>Laminae extending with little or no curvature or flexure</td>
      <td>Grey and Awramik (2020); p. 136; fig. 124</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesolamwaviness" data-status="provisional">
      <td class="domain">mesostructure, lamina waviness</td>
      <td class="term">Smooth</td>
      <td>Laminae lacking second-order curvature or flexures</td>
      <td>Grey and Awramik (2020); p. 136; fig. 124</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesolamwaviness" data-status="provisional">
      <td class="domain">mesostructure, lamina waviness</td>
      <td class="term">Crinkly</td>
      <td>Laminae displaying small-scale irregular wrinkles or crinkled flexures</td>
      <td>Grey and Awramik (2020); p. 136; fig. 124</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesolamwaviness" data-status="provisional">
      <td class="domain">mesostructure, lamina waviness</td>
      <td class="term">Wavy</td>
      <td>Laminae with regular second-order curvature and wavelengths commonly greater than 2 mm</td>
      <td>Grey and Awramik (2020); p. 136; fig. 124</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesolamwaviness" data-status="provisional">
      <td class="domain">mesostructure, lamina waviness</td>
      <td class="term">Undulatory</td>
      <td>Laminae showing broad smooth wave-like curvature across the profile</td>
      <td>Grey and Awramik (2020); p. 136; fig. 124</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesolatcontinuity" data-status="provisional">
      <td class="domain">mesostructure, lateral continuity</td>
      <td class="term">Continuous</td>
      <td>Laminae extending laterally without interruption across the microbialite</td>
      <td>Grey and Awramik (2020); p. 140; fig. 132</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesolatcontinuity" data-status="provisional">
      <td class="domain">mesostructure, lateral continuity</td>
      <td class="term">Discontinuous</td>
      <td>Laminae broken or interrupted laterally into separate segments</td>
      <td>Grey and Awramik (2020); p. 140; fig. 132</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesolatcontinuity" data-status="provisional">
      <td class="domain">mesostructure, lateral continuity</td>
      <td class="term">Lenticular</td>
      <td>Laminae occurring as lens-shaped discontinuous bodies</td>
      <td>Grey and Awramik (2020); p. 140; fig. 132</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesolatcontinuity" data-status="provisional">
      <td class="domain">mesostructure, lateral continuity</td>
      <td class="term">Micro-cross laminated</td>
      <td>Laminae displaying small-scale cross-laminated internal structure</td>
      <td>Grey and Awramik (2020); p. 140; fig. 132</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesolatcontinuity" data-status="provisional">
      <td class="domain">mesostructure, lateral continuity</td>
      <td class="term">Irregular</td>
      <td>Laminae with uneven thickness or irregular lateral persistence</td>
      <td>Grey and Awramik (2020); p. 140; fig. 132</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesolatcontinuity" data-status="provisional">
      <td class="domain">mesostructure, lateral continuity</td>
      <td class="term">Heterogeneous</td>
      <td>Laminae composed of mixed textures, structures, or continuity styles</td>
      <td>Grey and Awramik (2020); p. 140; fig. 132</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesolatcontinuity" data-status="provisional">
      <td class="domain">mesostructure, lateral continuity</td>
      <td class="term">Harmonized</td>
      <td>Laminae showing coordinated or parallel continuity patterns across adjacent layers</td>
      <td>Grey and Awramik (2020); p. 140; fig. 132</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesomacrolaminae" data-status="provisional">
      <td class="domain">mesostructure, macrolaminae</td>
      <td class="term">Alternating light/dark</td>
      <td>Macrolaminae composed of alternating light and dark layers</td>
      <td>Grey and Awramik (2020); p. 126; fig. 113</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesomacrolaminae" data-status="provisional">
      <td class="domain">mesostructure, macrolaminae</td>
      <td class="term">Predominantly light</td>
      <td>Macrolaminae dominated by light-colored laminae</td>
      <td>Grey and Awramik (2020); p. 126; fig. 113</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesomacrolaminae" data-status="provisional">
      <td class="domain">mesostructure, macrolaminae</td>
      <td class="term">Predominantly dark</td>
      <td>Macrolaminae dominated by dark-colored laminae</td>
      <td>Grey and Awramik (2020); p. 126; fig. 113</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesomacrolaminae" data-status="provisional">
      <td class="domain">mesostructure, macrolaminae</td>
      <td class="term">Intercalated minerals</td>
      <td>Macrolaminae containing distinct mineral intercalations between laminae</td>
      <td>Grey and Awramik (2020); p. 126; fig. 113</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesomacrolaminae" data-status="provisional">
      <td class="domain">mesostructure, macrolaminae</td>
      <td class="term">Progressive thickness change</td>
      <td>Macrolaminae showing systematic upward or downward changes in lamina thickness</td>
      <td>Grey and Awramik (2020); p. 126; fig. 113</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesomodalityskewness" data-status="provisional">
      <td class="domain">mesostructure, modality skewness</td>
      <td class="term">Unimodal</td>
      <td>Laminar profiles displaying a single dominant crest or mode</td>
      <td>Grey and Awramik (2020); p. 137; fig. 126</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesomodalityskewness" data-status="provisional">
      <td class="domain">mesostructure, modality skewness</td>
      <td class="term">Bimodal</td>
      <td>Laminar profiles displaying two dominant crests or modes</td>
      <td>Grey and Awramik (2020); p. 137; fig. 126</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesomodalityskewness" data-status="provisional">
      <td class="domain">mesostructure, modality skewness</td>
      <td class="term">Aysymmetric</td>
      <td>Laminar profiles displaying uneven or non-symmetrical crest distribution</td>
      <td>Grey and Awramik (2020); p. 137; fig. 126</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesomodalityskewness" data-status="provisional">
      <td class="domain">mesostructure, modality skewness</td>
      <td class="term">Multimodal</td>
      <td>Laminar profiles displaying multiple distinct crests or modes</td>
      <td>Grey and Awramik (2020); p. 137; fig. 126</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesooncoidflattening" data-status="provisional">
      <td class="domain">mesostructure, oncoid flattening</td>
      <td class="term">Equant</td>
      <td>Equant oncoids with approximately equal dimensions in all directions and little flattening</td>
      <td>Hickson</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesooncoidflattening" data-status="provisional">
      <td class="domain">mesostructure, oncoid flattening</td>
      <td class="term">Somewhat flattened</td>
      <td>Oncoids showing moderate compression along one axis while retaining a broadly rounded shape</td>
      <td>Hickson</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesooncoidflattening" data-status="provisional">
      <td class="domain">mesostructure, oncoid flattening</td>
      <td class="term">Flattened</td>
      <td>Oncoids strongly compressed along one axis, producing distinctly flattened morphologies</td>
      <td>Hickson</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesooncoids" data-status="provisional">
      <td class="domain">mesostructure, oncoids</td>
      <td class="term">Pisoid</td>
      <td>Rounded coated carbonate grain greater than 2 mm in diameter lacking visible concentric lamination or radial internal structure</td>
      <td>Hickson</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesooncoids" data-status="provisional">
      <td class="domain">mesostructure, oncoids</td>
      <td class="term">Pisoid, layered</td>
      <td>Rounded coated carbonate grain greater than 2 mm in diameter with distinct concentric lamination surrounding a nucleus</td>
      <td>Hickson</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesooncoids" data-status="provisional">
      <td class="domain">mesostructure, oncoids</td>
      <td class="term">Oncoid</td>
      <td>Irregularly shaped coated carbonate grain formed by microbial accretion around a nucleus</td>
      <td>Hickson</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesooncoids" data-status="provisional">
      <td class="domain">mesostructure, oncoids</td>
      <td class="term">Oncoid, layered</td>
      <td>Irregularly shaped coated carbonate grain with distinct concentric lamination surrounding a nucleus</td>
      <td>Hickson</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesooncoids" data-status="provisional">
      <td class="domain">mesostructure, oncoids</td>
      <td class="term">Oncoid, radial</td>
      <td>Irregularly shaped coated carbonate grain displaying internal radial structure extending outward from the nucleus</td>
      <td>Hickson</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesooncoidshape" data-status="provisional">
      <td class="domain">mesostructure, oncoid shape</td>
      <td class="term">Smooth</td>
      <td>Oncoids with smooth rounded margins and minimal surface irregularity</td>
      <td>Hickson</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesooncoidshape" data-status="provisional">
      <td class="domain">mesostructure, oncoid shape</td>
      <td class="term">Irregular</td>
      <td>Oncoids with uneven or variably lobed margins</td>
      <td>Hickson</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesooncoidshape" data-status="provisional">
      <td class="domain">mesostructure, oncoid shape</td>
      <td class="term">Very irregular</td>
      <td>Oncoids with strongly irregular, highly lobed, or jagged external morphology</td>
      <td>Hickson</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesostackingoverlap" data-status="provisional">
      <td class="domain">mesostructure, stacking overlap</td>
      <td class="term">Parallel</td>
      <td>Laminae terminate at the margin without overlapping adjacent laminae</td>
      <td>Grey and Awramik (2020); p. 117; fig. 111</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesostackingoverlap" data-status="provisional">
      <td class="domain">mesostructure, stacking overlap</td>
      <td class="term">Dark overlap</td>
      <td>Dark laminae preferentially overlap the terminations of adjacent laminae</td>
      <td>Grey and Awramik (2020); p. 117; fig. 111</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesostackingoverlap" data-status="provisional">
      <td class="domain">mesostructure, stacking overlap</td>
      <td class="term">Light overlap</td>
      <td>Light laminae preferentially overlap the terminations of adjacent laminae</td>
      <td>Grey and Awramik (2020); p. 117; fig. 111</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesosynopticrelief" data-status="provisional">
      <td class="domain">mesostructure, synoptic relief</td>
      <td class="term">Flat</td>
      <td>Synoptic relief between approximately 20 and 30 cm</td>
      <td>Grey and Awramik (2020); p. 138; fig. 128</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesosynopticrelief" data-status="provisional">
      <td class="domain">mesostructure, synoptic relief</td>
      <td class="term">Very low (&lt; 1 cm)</td>
      <td>Synoptic relief between approximately 30 and 50 cm</td>
      <td>Grey and Awramik (2020); p. 138; fig. 128</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesosynopticrelief" data-status="provisional">
      <td class="domain">mesostructure, synoptic relief</td>
      <td class="term">Low (&gt;1 - 2 cm)</td>
      <td>Synoptic relief absent or nearly absent with essentially planar laminae</td>
      <td>Grey and Awramik (2020); p. 138; fig. 128</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesosynopticrelief" data-status="provisional">
      <td class="domain">mesostructure, synoptic relief</td>
      <td class="term">Moderately low (&gt;2 - 5 cm)</td>
      <td>Synoptic relief less than approximately 1 cm</td>
      <td>Grey and Awramik (2020); p. 138; fig. 137</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesosynopticrelief" data-status="provisional">
      <td class="domain">mesostructure, synoptic relief</td>
      <td class="term">Moderate (&gt;5 - 10 cm)</td>
      <td>Synoptic relief between approximately 1 and 2 cm</td>
      <td>Grey and Awramik (2020); p. 138; fig. 128</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesosynopticrelief" data-status="provisional">
      <td class="domain">mesostructure, synoptic relief</td>
      <td class="term">Moderately high (&gt; 20 - 30 cm)</td>
      <td>Synoptic relief between approximately 2 and 5 cm</td>
      <td>Grey and Awramik (2020); p. 138; fig. 128</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesosynopticrelief" data-status="provisional">
      <td class="domain">mesostructure, synoptic relief</td>
      <td class="term">High (&gt;30 - 50 cm)</td>
      <td>Synoptic relief between approximately 5 and 10 cm</td>
      <td>Grey and Awramik (2020); p. 138; fig. 128</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesosynopticrelief" data-status="provisional">
      <td class="domain">mesostructure, synoptic relief</td>
      <td class="term">Very high (&gt; 50 cm)</td>
      <td>Synoptic relief greater than approximately 50 cm</td>
      <td>Grey and Awramik (2020); p. 138; fig. 128</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesotypes" data-status="obsolete">
      <td class="domain">mesostructure, types</td>
      <td class="term">Stromatolitic (laminated)</td>
      <td><em>Definition pending</em></td>
      <td></td>
      <td>obsolete</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesotypes" data-status="obsolete">
      <td class="domain">mesostructure, types</td>
      <td class="term">Concentric</td>
      <td><em>Definition pending</em></td>
      <td></td>
      <td>obsolete</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesotypes" data-status="obsolete">
      <td class="domain">mesostructure, types</td>
      <td class="term">Thrombolitic</td>
      <td><em>Definition pending</em></td>
      <td></td>
      <td>obsolete</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesotypes" data-status="obsolete">
      <td class="domain">mesostructure, types</td>
      <td class="term">Brecciated</td>
      <td><em>Definition pending</em></td>
      <td></td>
      <td>obsolete</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesotypes" data-status="obsolete">
      <td class="domain">mesostructure, types</td>
      <td class="term">Columnar</td>
      <td><em>Definition pending</em></td>
      <td></td>
      <td>obsolete</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesotypes" data-status="obsolete">
      <td class="domain">mesostructure, types</td>
      <td class="term">Digitate</td>
      <td><em>Definition pending</em></td>
      <td></td>
      <td>obsolete</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesotypes" data-status="obsolete">
      <td class="domain">mesostructure, types</td>
      <td class="term">Oncolitic</td>
      <td><em>Definition pending</em></td>
      <td></td>
      <td>obsolete</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesotypes" data-status="obsolete">
      <td class="domain">mesostructure, types</td>
      <td class="term">Pisolitic</td>
      <td><em>Definition pending</em></td>
      <td></td>
      <td>obsolete</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesotypes" data-status="obsolete">
      <td class="domain">mesostructure, types</td>
      <td class="term">Massive</td>
      <td><em>Definition pending</em></td>
      <td></td>
      <td>obsolete</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesotypes" data-status="obsolete">
      <td class="domain">mesostructure, types</td>
      <td class="term">Radial</td>
      <td><em>Definition pending</em></td>
      <td></td>
      <td>obsolete</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesowalls" data-status="provisional">
      <td class="domain">mesostructure, walls</td>
      <td class="term">Unwalled</td>
      <td>Microbialites lacking distinct wall structures along lamina margins</td>
      <td>Grey and Awramik (2020); p. 145; fig. 137</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesowalls" data-status="provisional">
      <td class="domain">mesostructure, walls</td>
      <td class="term">Simple</td>
      <td>Microbialites with a single well-defined wall bordering the laminae</td>
      <td>Grey and Awramik (2020); p. 145; fig. 137</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesowalls" data-status="provisional">
      <td class="domain">mesostructure, walls</td>
      <td class="term">Multilaminate</td>
      <td>Microbialites with walls composed of multiple closely spaced laminae</td>
      <td>Grey and Awramik (2020); p. 145; fig. 137</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesowalls" data-status="provisional">
      <td class="domain">mesostructure, walls</td>
      <td class="term">Patchy</td>
      <td>Microbialites with discontinuous or irregularly developed wall structures</td>
      <td>Grey and Awramik (2020); p. 145; fig. 137</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesowalls" data-status="provisional">
      <td class="domain">mesostructure, walls</td>
      <td class="term">Complex</td>
      <td>Microbialites with highly irregular or composite wall structures showing multiple morphologies</td>
      <td>Grey and Awramik (2020); p. 145; fig. 137</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmesowalls" data-status="provisional">
      <td class="domain">mesostructure, walls</td>
      <td class="term">Selvage</td>
      <td>A marginal border or fringe developed along the outer edge of the microbialite wall</td>
      <td>Grey and Awramik (2020); p. 145; fig. 137</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrocarbonategrains" data-status="provisional">
      <td class="domain">microstructure, carbonate grains</td>
      <td class="term">Skeletal grains</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrocarbonategrains" data-status="provisional">
      <td class="domain">microstructure, carbonate grains</td>
      <td class="term">Ooids</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrocarbonategrains" data-status="provisional">
      <td class="domain">microstructure, carbonate grains</td>
      <td class="term">Pisoids</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrocarbonategrains" data-status="provisional">
      <td class="domain">microstructure, carbonate grains</td>
      <td class="term">Oncoids</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrocarbonategrains" data-status="provisional">
      <td class="domain">microstructure, carbonate grains</td>
      <td class="term">Peloids</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrocarbonategrains" data-status="provisional">
      <td class="domain">microstructure, carbonate grains</td>
      <td class="term">Intraclasts</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrocarbonategrains" data-status="provisional">
      <td class="domain">microstructure, carbonate grains</td>
      <td class="term">Micrite</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrocementtypes" data-status="provisional">
      <td class="domain">microstructure, cement types</td>
      <td class="term">Isopachous</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrocementtypes" data-status="provisional">
      <td class="domain">microstructure, cement types</td>
      <td class="term">Radial fibrous</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrocementtypes" data-status="provisional">
      <td class="domain">microstructure, cement types</td>
      <td class="term">Mosaic (vadose?)</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrocementtypes" data-status="provisional">
      <td class="domain">microstructure, cement types</td>
      <td class="term">Pendant</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrocementtypes" data-status="provisional">
      <td class="domain">microstructure, cement types</td>
      <td class="term">Meniscus</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrocementtypes" data-status="provisional">
      <td class="domain">microstructure, cement types</td>
      <td class="term">Botryoidal</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrocementtypes" data-status="provisional">
      <td class="domain">microstructure, cement types</td>
      <td class="term">Isopachous Botryoidal</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrocementtypes" data-status="provisional">
      <td class="domain">microstructure, cement types</td>
      <td class="term">Isopachous Fibrous</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrocementtypes" data-status="provisional">
      <td class="domain">microstructure, cement types</td>
      <td class="term">Isopachous Sparry</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrocementtypes" data-status="provisional">
      <td class="domain">microstructure, cement types</td>
      <td class="term">Isopachous Acicular</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrocementtypes" data-status="provisional">
      <td class="domain">microstructure, cement types</td>
      <td class="term">Isopachous Bladed</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrocementtypes" data-status="provisional">
      <td class="domain">microstructure, cement types</td>
      <td class="term">Dog-tooth spar</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrocementtypes" data-status="provisional">
      <td class="domain">microstructure, cement types</td>
      <td class="term">Calcite spar (drusy)</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrocementtypes" data-status="provisional">
      <td class="domain">microstructure, cement types</td>
      <td class="term">Herringbone</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicroclasticgrains" data-status="provisional">
      <td class="domain">microstructure, clastic grains</td>
      <td class="term">Monocrystalline Quartz</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicroclasticgrains" data-status="provisional">
      <td class="domain">microstructure, clastic grains</td>
      <td class="term">Polycrystalline Quartz</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicroclasticgrains" data-status="provisional">
      <td class="domain">microstructure, clastic grains</td>
      <td class="term">Microcrystalline Quarz (chert)</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicroclasticgrains" data-status="provisional">
      <td class="domain">microstructure, clastic grains</td>
      <td class="term">Feldspar undifferentiated</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicroclasticgrains" data-status="provisional">
      <td class="domain">microstructure, clastic grains</td>
      <td class="term">K-spar</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicroclasticgrains" data-status="provisional">
      <td class="domain">microstructure, clastic grains</td>
      <td class="term">Plagioclase</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicroclasticgrains" data-status="provisional">
      <td class="domain">microstructure, clastic grains</td>
      <td class="term">Lithic volcanic</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicroclasticgrains" data-status="provisional">
      <td class="domain">microstructure, clastic grains</td>
      <td class="term">Lithic sedimentary</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicroclasticgrains" data-status="provisional">
      <td class="domain">microstructure, clastic grains</td>
      <td class="term">Lithic metamorphic</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicromicrofacies" data-status="provisional">
      <td class="domain">microstructure, microfacies</td>
      <td class="term">Continuous microlaminae: carbon-rich/cement alternation</td>
      <td><em>Definition pending</em></td>
      <td></td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicromicrofacies" data-status="provisional">
      <td class="domain">microstructure, microfacies</td>
      <td class="term">Continuous microlaminae: isopachous cement dominant</td>
      <td><em>Definition pending</em></td>
      <td></td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicromineralogy" data-status="provisional">
      <td class="domain">microstructure, mineralogy</td>
      <td class="term">Selenite</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicromineralogy" data-status="provisional">
      <td class="domain">microstructure, mineralogy</td>
      <td class="term">Siderite</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicromineralogy" data-status="provisional">
      <td class="domain">microstructure, mineralogy</td>
      <td class="term">Magnesite</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicromineralogy" data-status="provisional">
      <td class="domain">microstructure, mineralogy</td>
      <td class="term">Halite</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicromineralogy" data-status="provisional">
      <td class="domain">microstructure, mineralogy</td>
      <td class="term">Barite</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicromineralogy" data-status="provisional">
      <td class="domain">microstructure, mineralogy</td>
      <td class="term">Calcite (undiff.)</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicromineralogy" data-status="provisional">
      <td class="domain">microstructure, mineralogy</td>
      <td class="term">Aragonite</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicromineralogy" data-status="provisional">
      <td class="domain">microstructure, mineralogy</td>
      <td class="term">Dolomite</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicromineralogy" data-status="provisional">
      <td class="domain">microstructure, mineralogy</td>
      <td class="term">Chert</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicromineralogy" data-status="provisional">
      <td class="domain">microstructure, mineralogy</td>
      <td class="term">Macrocrystalline Qtz</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicromineralogy" data-status="provisional">
      <td class="domain">microstructure, mineralogy</td>
      <td class="term">Quartz</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicromineralogy" data-status="provisional">
      <td class="domain">microstructure, mineralogy</td>
      <td class="term">Pyrite</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicromineralogy" data-status="provisional">
      <td class="domain">microstructure, mineralogy</td>
      <td class="term">Gypsum (undiff.)</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicromineralogy" data-status="provisional">
      <td class="domain">microstructure, mineralogy</td>
      <td class="term">Anhydrite</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicropercentclastics" data-status="provisional">
      <td class="domain">microstructure, percent clastics</td>
      <td class="term">1%</td>
      <td><em>Definition pending</em></td>
      <td>Database operational terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicropercentclastics" data-status="provisional">
      <td class="domain">microstructure, percent clastics</td>
      <td class="term">Patchy (11-50%)</td>
      <td><em>Definition pending</em></td>
      <td>Database operational terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicropercentclastics" data-status="provisional">
      <td class="domain">microstructure, percent clastics</td>
      <td class="term">Broken (51-90%)</td>
      <td><em>Definition pending</em></td>
      <td>Database operational terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicropercentclastics" data-status="provisional">
      <td class="domain">microstructure, percent clastics</td>
      <td class="term">Continuous (91-100%)</td>
      <td><em>Definition pending</em></td>
      <td>Database operational terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicropercentclastics" data-status="provisional">
      <td class="domain">microstructure, percent clastics</td>
      <td class="term">3%</td>
      <td><em>Definition pending</em></td>
      <td>Database operational terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicropercentclastics" data-status="provisional">
      <td class="domain">microstructure, percent clastics</td>
      <td class="term">5%</td>
      <td><em>Definition pending</em></td>
      <td>Database operational terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicropercentclastics" data-status="provisional">
      <td class="domain">microstructure, percent clastics</td>
      <td class="term">10%</td>
      <td><em>Definition pending</em></td>
      <td>Database operational terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicropercentclastics" data-status="provisional">
      <td class="domain">microstructure, percent clastics</td>
      <td class="term">20%</td>
      <td><em>Definition pending</em></td>
      <td>Database operational terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicropercentclastics" data-status="provisional">
      <td class="domain">microstructure, percent clastics</td>
      <td class="term">30%</td>
      <td><em>Definition pending</em></td>
      <td>Database operational terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicropercentclastics" data-status="provisional">
      <td class="domain">microstructure, percent clastics</td>
      <td class="term">40%</td>
      <td><em>Definition pending</em></td>
      <td>Database operational terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicropercentclastics" data-status="provisional">
      <td class="domain">microstructure, percent clastics</td>
      <td class="term">50%</td>
      <td><em>Definition pending</em></td>
      <td>Database operational terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicropercentclastics" data-status="provisional">
      <td class="domain">microstructure, percent clastics</td>
      <td class="term">Sporadic (1-10%)</td>
      <td><em>Definition pending</em></td>
      <td>Database operational terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicroporositydirection" data-status="provisional">
      <td class="domain">microstructure, porosity direction</td>
      <td class="term">Enlarged</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicroporositydirection" data-status="provisional">
      <td class="domain">microstructure, porosity direction</td>
      <td class="term">Reduced</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicroporositydirection" data-status="provisional">
      <td class="domain">microstructure, porosity direction</td>
      <td class="term">Filled</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicroporosityprocess" data-status="provisional">
      <td class="domain">microstructure, porosity process</td>
      <td class="term">Solution</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicroporosityprocess" data-status="provisional">
      <td class="domain">microstructure, porosity process</td>
      <td class="term">Cementation</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicroporosityprocess" data-status="provisional">
      <td class="domain">microstructure, porosity process</td>
      <td class="term">Internal sediment</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicroporositysize" data-status="provisional">
      <td class="domain">microstructure, porosity size</td>
      <td class="term">Megapore (4-256mm)</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicroporositysize" data-status="provisional">
      <td class="domain">microstructure, porosity size</td>
      <td class="term">Mesopore (0.0625-4mm)</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicroporositysize" data-status="provisional">
      <td class="domain">microstructure, porosity size</td>
      <td class="term">Micropore (&lt;0.0625mm)</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicroporositytypes" data-status="provisional">
      <td class="domain">microstructure, porosity types</td>
      <td class="term">NFS: Channel</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicroporositytypes" data-status="provisional">
      <td class="domain">microstructure, porosity types</td>
      <td class="term">NFS: Vug or macroporous</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicroporositytypes" data-status="provisional">
      <td class="domain">microstructure, porosity types</td>
      <td class="term">NFS: Cavern</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicroporositytypes" data-status="provisional">
      <td class="domain">microstructure, porosity types</td>
      <td class="term">FS or NFS: Breccia</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicroporositytypes" data-status="provisional">
      <td class="domain">microstructure, porosity types</td>
      <td class="term">FS or NFS: Boring</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicroporositytypes" data-status="provisional">
      <td class="domain">microstructure, porosity types</td>
      <td class="term">FS or NFS: Burrow</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicroporositytypes" data-status="provisional">
      <td class="domain">microstructure, porosity types</td>
      <td class="term">FS or NFS: Shrinkage</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicroporositytypes" data-status="provisional">
      <td class="domain">microstructure, porosity types</td>
      <td class="term">FS: Interparticle</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicroporositytypes" data-status="provisional">
      <td class="domain">microstructure, porosity types</td>
      <td class="term">FS: Intraparticle</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicroporositytypes" data-status="provisional">
      <td class="domain">microstructure, porosity types</td>
      <td class="term">FS: Growth-framework</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicroporositytypes" data-status="provisional">
      <td class="domain">microstructure, porosity types</td>
      <td class="term">FS: Shelter</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicroporositytypes" data-status="provisional">
      <td class="domain">microstructure, porosity types</td>
      <td class="term">FS: Fenestral</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicroporositytypes" data-status="provisional">
      <td class="domain">microstructure, porosity types</td>
      <td class="term">FS Secondary: Inter-crystal</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicroporositytypes" data-status="provisional">
      <td class="domain">microstructure, porosity types</td>
      <td class="term">FS Secondary: Mouldic</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicroporositytypes" data-status="provisional">
      <td class="domain">microstructure, porosity types</td>
      <td class="term">NFS: Fracture</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrotexturetypes" data-status="provisional">
      <td class="domain">microstructure, texture types</td>
      <td class="term">Massive micritic</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrotexturetypes" data-status="provisional">
      <td class="domain">microstructure, texture types</td>
      <td class="term">Microfossiliferous</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrotexturetypes" data-status="provisional">
      <td class="domain">microstructure, texture types</td>
      <td class="term">Grumous</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrotexturetypes" data-status="provisional">
      <td class="domain">microstructure, texture types</td>
      <td class="term">Recrystallized</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrotexturetypes" data-status="provisional">
      <td class="domain">microstructure, texture types</td>
      <td class="term">Peloidal</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrotexturetypes" data-status="provisional">
      <td class="domain">microstructure, texture types</td>
      <td class="term">Microlaminated</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrotexturetypes" data-status="provisional">
      <td class="domain">microstructure, texture types</td>
      <td class="term">Granular</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrotexturetypes" data-status="provisional">
      <td class="domain">microstructure, texture types</td>
      <td class="term">Oolitic</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrotexturetypes" data-status="provisional">
      <td class="domain">microstructure, texture types</td>
      <td class="term">Fibrous</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrotexturetypes" data-status="provisional">
      <td class="domain">microstructure, texture types</td>
      <td class="term">Cement</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrotexturetypes" data-status="provisional">
      <td class="domain">microstructure, texture types</td>
      <td class="term">Spherical</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrowentworth" data-status="provisional">
      <td class="domain">microstructure, Wentworth size class</td>
      <td class="term">Clay</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrowentworth" data-status="provisional">
      <td class="domain">microstructure, Wentworth size class</td>
      <td class="term">Cobble</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrowentworth" data-status="provisional">
      <td class="domain">microstructure, Wentworth size class</td>
      <td class="term">&gt; Cobble</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrowentworth" data-status="provisional">
      <td class="domain">microstructure, Wentworth size class</td>
      <td class="term">Silt</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrowentworth" data-status="provisional">
      <td class="domain">microstructure, Wentworth size class</td>
      <td class="term">Vf Sand</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrowentworth" data-status="provisional">
      <td class="domain">microstructure, Wentworth size class</td>
      <td class="term">F sand</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrowentworth" data-status="provisional">
      <td class="domain">microstructure, Wentworth size class</td>
      <td class="term">M sand</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrowentworth" data-status="provisional">
      <td class="domain">microstructure, Wentworth size class</td>
      <td class="term">C sand</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrowentworth" data-status="provisional">
      <td class="domain">microstructure, Wentworth size class</td>
      <td class="term">Vc sand</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrowentworth" data-status="provisional">
      <td class="domain">microstructure, Wentworth size class</td>
      <td class="term">Granule</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpmicrowentworth" data-status="provisional">
      <td class="domain">microstructure, Wentworth size class</td>
      <td class="term">Pebble</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpprojecttectonicsetting" data-status="provisional">
      <td class="domain">project, tectonic setting</td>
      <td class="term">Epeiric sea</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpprojecttectonicsetting" data-status="provisional">
      <td class="domain">project, tectonic setting</td>
      <td class="term">Ramp</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpprojecttectonicsetting" data-status="provisional">
      <td class="domain">project, tectonic setting</td>
      <td class="term">Rimmed platform</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpprojecttectonicsetting" data-status="provisional">
      <td class="domain">project, tectonic setting</td>
      <td class="term">Intracontinental basin</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpprojecttectonicsetting" data-status="provisional">
      <td class="domain">project, tectonic setting</td>
      <td class="term">Foreland basin</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpprojecttectonicsetting" data-status="provisional">
      <td class="domain">project, tectonic setting</td>
      <td class="term">Forearc basin</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpprojecttectonicsetting" data-status="provisional">
      <td class="domain">project, tectonic setting</td>
      <td class="term">Rift basin</td>
      <td><em>Definition pending</em></td>
      <td>Standard sedimentological terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpsemandotherdatatypes" data-status="provisional">
      <td class="domain">SEM and other data types</td>
      <td class="term">SEM on thick section</td>
      <td><em>Definition pending</em></td>
      <td>Database operational terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpsemandotherdatatypes" data-status="provisional">
      <td class="domain">SEM and other data types</td>
      <td class="term">SEM on peel</td>
      <td><em>Definition pending</em></td>
      <td>Database operational terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpsemandotherdatatypes" data-status="provisional">
      <td class="domain">SEM and other data types</td>
      <td class="term">SEM on polished thin section</td>
      <td><em>Definition pending</em></td>
      <td>Database operational terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkpsemandotherdatatypes" data-status="provisional">
      <td class="domain">SEM and other data types</td>
      <td class="term">SEM on mounted fragment</td>
      <td><em>Definition pending</em></td>
      <td>Database operational terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkptrait_observation_quality" data-status="provisional">
      <td class="domain">trait observation quality</td>
      <td class="term">Observed</td>
      <td><em>Definition pending</em></td>
      <td>Database operational terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkptrait_observation_quality" data-status="provisional">
      <td class="domain">trait observation quality</td>
      <td class="term">Poor image quality</td>
      <td><em>Definition pending</em></td>
      <td>Database operational terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkptrait_observation_quality" data-status="provisional">
      <td class="domain">trait observation quality</td>
      <td class="term">Insufficient Resolution</td>
      <td><em>Definition pending</em></td>
      <td>Database operational terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkptrait_observation_quality" data-status="provisional">
      <td class="domain">trait observation quality</td>
      <td class="term">Incomplete Data</td>
      <td><em>Definition pending</em></td>
      <td>Database operational terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkptrait_observation_quality" data-status="provisional">
      <td class="domain">trait observation quality</td>
      <td class="term">Not preserved</td>
      <td><em>Definition pending</em></td>
      <td>Database operational terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkptrait_observation_quality" data-status="provisional">
      <td class="domain">trait observation quality</td>
      <td class="term">Not Exposed</td>
      <td><em>Definition pending</em></td>
      <td>Database operational terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkptrait_observation_quality" data-status="provisional">
      <td class="domain">trait observation quality</td>
      <td class="term">Obscured</td>
      <td><em>Definition pending</em></td>
      <td>Database operational terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkptrait_observation_quality" data-status="provisional">
      <td class="domain">trait observation quality</td>
      <td class="term">Uncertain</td>
      <td><em>Definition pending</em></td>
      <td>Database operational terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkptrait_observation_quality" data-status="provisional">
      <td class="domain">trait observation quality</td>
      <td class="term">Inferred</td>
      <td><em>Definition pending</em></td>
      <td>Database operational terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    <tr data-domain="tlkptrait_observation_quality" data-status="provisional">
      <td class="domain">trait observation quality</td>
      <td class="term">Ambiguous</td>
      <td><em>Definition pending</em></td>
      <td>Database operational terminology</td>
      <td>provisional</td>
      <td></td>
    </tr>
    </tbody>
  </table>
</div>

<script>
function filterVocab() {
  var search = document.getElementById("vocabSearch").value.toLowerCase();
  var domain = document.getElementById("domainFilter").value;
  var status = document.getElementById("statusFilter").value;
  var rows = document.querySelectorAll("#vocabTable tbody tr");

  rows.forEach(function(row) {
    var rowText = row.innerText.toLowerCase();
    var rowDomain = row.getAttribute("data-domain");
    var rowStatus = row.getAttribute("data-status");

    var matchesSearch = rowText.indexOf(search) > -1;
    var matchesDomain = !domain || rowDomain === domain;
    var matchesStatus = !status || rowStatus === status;

    row.style.display = (matchesSearch && matchesDomain && matchesStatus) ? "" : "none";
  });
}
</script>
