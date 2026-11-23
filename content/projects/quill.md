---
title: Quill
projectKind: case-study
caption: A dialogue editor that gives writers a way to check their own changes
  in Unreal.
image: images/quill_project-image_1800x1200.jpg
alt: Quill's node-graph dialogue editor inside Unreal, showing a branching
  conversation beside a list of lines that still need translations.
year: 2025–present
role: Sole developer
tags:
  - Unreal
  - C++
  - Slate
  - tools
sections:
  - heading: Problem
    text: On student teams, writers draft dialogue in Google Docs and a programmer
      copies it by hand into Unreal's Data Tables. Lines get mistyped, quest
      flags break and revisions go missing. I first saw it during my IMS213 lab
      hours in fall 2025 and started the importer that semester.
  - heading: My role
    text: "Sole developer. I wrote the Unreal editor plugin in C++ with a Slate
      interface: a node-graph dialogue editor, conditions and flags, CSV and
      JSON import from spreadsheets, and a missing-line report for
      localization."
  - heading: Research
    image: images/quill_section-research_1200x900.jpg
    alt: "Notes from a usability test: a writer at a laptop beside a sheet of
      observations from five sessions."
    text: >-
      I tested an early version with five writers, using the methods from IMS314
      Game Usability.


      “The writer changed one line. I had to open Unreal to tell her whether it
      had made it into the game. That was the part I wanted to get rid of.” One
      writer finished an import, saw “1 missing translation” and asked me which
      line. The importer knew the answer. I'd left it out of the interface.
  - heading: Prototype
    image: images/quill_section-prototype_900x1200.jpg
    alt: Pencil sketches of Quill's editor window, with sticky notes standing in for
      dialogue nodes.
    text: Before writing any Slate code, I sketched the editor window on paper and
      walked writers through it, moving sticky notes around as dialogue nodes.
  - heading: Iteration
    image: images/quill_section-iteration_1200x600.jpg
    alt: "Before and after: a line of dialogue in a spreadsheet, and the same line
      arriving in a Quill dialogue node."
    text: In the demo I follow one line from the spreadsheet into a dialogue node,
      then show where the writer can see that its translation is missing. The
      missing-line report checks the data at edit time, so she can check her own
      change. In the sample sheet, KEEP_014 changes from “Leave the lamp
      burning” to “Leave the west lamp burning.” The writer can move the row
      without breaking the branch because I match on its ID. Selecting the
      warning now focuses that node and shows the empty French field. The writer
      supplied the dialogue; I wrote the import and selection behavior.
  - heading: Outcome
    image: images/quill_section-outcome_1200x750.jpg
    alt: Quill's missing-line report, listing dialogue lines that have no
      translation yet.
    text: Two other Miami student teams used Quill. When my IMS489 team started
      Tidewatch in fall 2026, the same problem arrived at full scale, and
      Tidewatch became Quill's largest user.
  - heading: Reflection
    text: Quill has no runtime localization yet, and the Slate code needs a refactor
      I've been putting off. Both are open work.
weight: 1
---
Quill is a dialogue and quest-data editor for Unreal Engine 5. It lets a writer change a line and see for herself whether the change made it into the game, without asking a programmer.