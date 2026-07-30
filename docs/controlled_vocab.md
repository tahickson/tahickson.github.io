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

  .schema-button {
    display: inline-block;
    padding: 0.7rem 1rem;
    border-radius: 0.45rem;
    background: #1677a3;
    color: white;
    font-weight: 650;
    text-decoration: none;
  }

  .schema-button:hover,
  .schema-button:focus {
    color: white;
    background: #105f83;
  }
</style>

<h1>Controlled Vocabulary</h1>

<div class="vocab-intro" markdown="0">
  <p>
    The Microbial Biosignatures Project maintains its controlled vocabulary in
    a dedicated PostgreSQL schema. The schema documents the terms, definitions,
    sources, statuses, and relationships used by the microbialites database.
  </p>

  <div class="vocab-callout">
    <strong>Current status:</strong> preliminary working vocabulary. Terms and
    definitions are being reviewed as the database structure and community
    feedback evolve.
  </div>

  <p>
    Browse the live database structure, tables, columns, and relationships in
    the SchemaSpy report.
  </p>

  <p>
    <a class="schema-button" href="{{ '/vocabulary-schema/latest/' | relative_url }}">
      View controlled vocabulary schema
    </a>
  </p>
</div>
