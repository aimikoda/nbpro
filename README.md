# Nano Banana Pro (Gemini 3 Pro Image) — Usage Guide & Prompting Tips

This document merges the practical usage notes and prompting guidance from Google’s official posts about **Nano Banana Pro (Gemini 3 Pro Image)** into a single, ready-to-use reference.

---

## Table of contents
- [1. What is Nano Banana Pro?](#1-what-is-nano-banana-pro)
- [2. Where can you use it?](#2-where-can-you-use-it)
- [3. Key strengths](#3-key-strengths)
- [4. A reliable prompt structure](#4-a-reliable-prompt-structure)
- [5. Seven practical techniques (with examples)](#5-seven-practical-techniques-with-examples)
- [6. Image editing rules of thumb](#6-image-editing-rules-of-thumb)
- [7. Limitations and quality checks](#7-limitations-and-quality-checks)
- [8. Copy-paste prompt templates](#8-copy-paste-prompt-templates)
- [9. Transparency note (SynthID and labeling)](#9-transparency-note-synthid-and-labeling)

---

## 1. What is Nano Banana Pro?

**Nano Banana Pro** is Google DeepMind’s image generation and image editing model built on **Gemini 3 Pro**. It is positioned for tasks where you want more “reasoning” and better use of real-world context, including prototyping, diagrams, infographics, and creative design work.

Typical goals:
- Visualize ideas, turn notes into diagrams, generate data-driven infographics
- Place **readable, accurate text** inside images (from short slogans to longer blocks)
- Support **multilingual** text creation and localization
- Combine multiple inputs while aiming for **character and scene consistency**

---

## 2. Where can you use it?

Availability can vary by product surface and rollout phase. In Google’s posts, usage is described across a few major surfaces, including:
- The **Gemini app**, where you can select image creation with a “Thinking” model (and some experiences can fall back to the original Nano Banana when limits are reached)
- **NotebookLM** (noted for subscribers)
- **Google Ads** and **Workspace** experiences like Slides/Vids (for professional use)
- **Developer and enterprise** surfaces such as Gemini API / Google AI Studio and Vertex AI

---

## 3. Key strengths

### 3.1 Real-world grounding for richer visuals
Nano Banana Pro is presented as aiming for more context-rich outputs. Some experiences can be grounded in up-to-date information (depending on the product surface).

### 3.2 Strong in-image text and multilingual support
A headline feature is producing **cleaner, more readable in-image typography**, plus translation and localization workflows.

### 3.3 Multi-image inputs and compositional consistency
The model is described as able to blend multiple sources and keep identity cues more consistent (limits depend on the surface).

### 3.4 “Studio controls”: lighting, focus, grading, time-of-day
Editing examples include targeted changes like shifting lighting mood, focus, color grading, or day-to-night transformations.

### 3.5 Output formats and aspect ratios
Guidance emphasizes controlling aspect ratio (9:16, 1:1, 16:9, etc.) and, where available, choosing higher resolution outputs.

---

## 4. A reliable prompt structure

A practical “always works” prompt checklist:

1) **Subject**: what/who is in the image  
2) **Composition**: framing, angle, distance, lens vibe  
3) **Action**: what is happening  
4) **Location**: where/when  
5) **Style**: aesthetics (photoreal, illustration, film noir, etc.)

Then add “pro” details:
- **Aspect ratio** and output intent (poster, thumbnail, storyboard frame, etc.)
- **Lighting** (type, direction, atmosphere)
- **Text instructions** (exact text, placement, typographic feel)
- **Accuracy constraints** (especially for infographics and technical diagrams)
- **Reference roles** when you provide multiple images (A = pose, B = style, C = background)

---

## 5. Seven practical techniques (with examples)

### 1) Lean into in-image text (posters, mockups, diagrams)
Specify the exact text, its placement, and readability requirements.

**Example**
> Create a minimalist poster. Title text at the top: “WINTER EDITION”. Use clean sans-serif typography, high contrast, perfectly readable, no misspellings. 9:16.

### 2) Use real-world structure for explanatory infographics
Ask for sections, hierarchy, and clarity.

**Example**
> Create an infographic about espresso extraction. Sections: grind size, water temperature, ratio, time, common mistakes. Clear typographic hierarchy, accurate terminology, neat layout.

### 3) Translation/localization edits
Make “only text changes” explicit.

**Example**
> Translate all English text in the image to Turkish. Keep layout, colors, icons, and composition unchanged. Only replace text. Ensure no overflow and perfect readability.

### 4) Studio-style edits: lighting, focus, mood, grading
Target a single change with strong constraints.

**Example**
> Keep everything the same, but change the scene to nighttime with soft street lights. Preserve subject identity and pose. Maintain realism.

### 5) Resize and reframe for new aspect ratios
Ask for a careful reframe rather than a redesign.

**Example**
> Convert to 1:1. Keep the subject scale and position similar. Recompose the background to fit without cropping important elements.

### 6) Blend multiple images with explicit roles
Tell the model exactly what comes from where.

**Example**
> Image A provides the pose, Image B provides the wardrobe style, Image C provides the background. Combine into a single coherent scene with consistent lighting and perspective.

### 7) Lock a brand “look and feel”
Standardize palette, typography, and materials.

**Example**
> Use a consistent brand style: warm beige background, charcoal text, subtle grain, modern editorial layout, clean sans-serif type, generous whitespace.

---

## 6. Image editing rules of thumb

When editing an existing image, give instructions that are:
- **Direct**: what changes
- **Constrained**: what must not change
- **Localized**: where the change applies

A simple checklist:
- “**Only X changes**; everything else stays the same.”
- For text: include **exact replacement text**, placement constraints, and “no overflow”.
- For lighting/color: specify mood, direction, and intensity.
- If consistency matters: call out identity markers to preserve (face, pose, accessories).

---

## 7. Limitations and quality checks

Even with strong prompting, you should review outputs carefully, especially when:
- Text is small or dense (watch for typos or warped letters)
- Diagrams/infographics require factual accuracy (verify numbers, labels, terminology)
- Translation requires nuance (grammar and cultural phrasing may need human review)
- Heavy blending/complex edits can introduce artifacts
- Character consistency must be preserved across multiple iterations

---

## 8. Copy-paste prompt templates

### 8.1 New image generation (general)
**Subject:** …  
**Composition:** …  
**Action:** …  
**Location:** …  
**Style:** …  
**Lighting:** …  
**Output:** aspect ratio …, intended use …

### 8.2 Text-first poster / mockup
> [Scene description]. Add this exact text: “…” at [top/center/bottom]. Clean [typography style], high contrast, perfectly readable, no misspellings, no cropping. Aspect ratio: [9:16].

### 8.3 Diagram / infographic with accuracy constraints
> Create an infographic about [topic]. Sections: [list]. Use accurate terminology and consistent numbers. Clear typographic hierarchy. Readable labels, neat grid layout.

### 8.4 In-image text translation (edit)
> Translate all text in the image from [source language] to [target language]. Keep layout, colors, icons, and composition the same. Only text changes. No overflow, fully readable.

### 8.5 Aspect ratio conversion (edit)
> Change aspect ratio to [1:1]. Keep subject scale/pose consistent. Recompose background to fit. Do not alter identity or styling.

### 8.6 Multi-image blend with roles
> Image A = pose. Image B = style. Image C = background. Combine into one coherent scene. Preserve identity cues. Match lighting and perspective. Aspect ratio: [16:9].

---

## 9. Transparency note (SynthID and labeling)

Google notes that media generated with Google tools may include **SynthID** watermarking and that some experiences may label AI-generated outputs.

### Source note

This document is a consolidated and independently written guide based on information published by Google about Nano Banana Pro (Gemini 3 Pro Image).

It was compiled from the following official sources:
- Google Technology Blog: Nano Banana Pro overview and capabilities  
- Google Gemini Blog: Prompting tips and best practices for Nano Banana Pro

The content has been reorganized, summarized, and rewritten for clarity and practical use.  
It is intended as an educational and reference resource and is not an official Google publication.


