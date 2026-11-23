---
title: Heatcheck
projectKind: project
caption: Playtest telemetry for Unity · C# and Python · IMS314 Game Usability
image: images/heatcheck_project-image_1800x1200.jpg
alt: A heatmap of player positions laid over the top-down map of a student game
  level.
year: "2026"
role: Sole developer
tags:
  - Unity
  - C#
  - Python
  - playtesting
sections:
  - heading: Heatmaps and death maps
    image: images/heatcheck_section-heatmaps_1200x1200.jpg
    alt: A death map from a playtest, with clusters of markers where players fell.
    text: The Python script (pandas and matplotlib) draws where players went and
      where they died, over a top-down image of the level.
  - heading: What a heatmap doesn't tell you
    text: I wrote a one-page method note to go with the tool. A heatmap shows where
      players were, not why they were there or what they were trying to do. One
      gate looked like a bottleneck until we lined up the pause with the
      gate-open event. The gate was already open. The observer had written,
      “Went back to watch the platform.” That became the worked example on my
      method sheet.
weight: 3
---
Heatcheck is a drop-in C# package for Unity that logs player positions and custom events to JSON. A Python script turns the logs into heatmaps and death maps. My IMS314 class used it in usability studies of three student games.