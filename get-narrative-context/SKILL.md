---
name: get-narrative-context
description: Use when you need to understand an existing narrative structure, characters, locations, or scene organization. Generic guide for reading and referencing narrative context in any project.
when_to_use: |
  - Starting with fresh conversation context and have no prior narrative knowledge
  - Need to understand character details and relationships
  - Need to understand location details and geography
  - Need to find existing scenes or chapters
  - Need to understand narrative hierarchy (parts, books, chapters, scenes)
  - Creating or modifying narrative content in a narrative project
---

# How to Get Context About an Existing Narrative

## Building Full Narrative Context

**ALWAYS read scenes AND get character AND location context together:**

1. **Start by identifying scene structure** — know where to find scenes
2. **Read actual scene files** to understand narrative, character names, and settings
3. **Get character context** — read people files or extract from scenes
4. **Get location context** — read location files or extract from scenes
5. **Cross-reference everything** — compare info from scenes with people/location files for consistency
6. **Build comprehensive understanding** of characters, relationships, locations, and story flow before creating or modifying content

## Understanding Scene Structure

**Hierarchy Levels** (from smallest to largest): Scenes < Chapters < Parts < Books

**Flexible Nesting**: Any organizational level can internally contain any level below it. For example, a Part can contain Chapters, Scenes directly, or Books. Books, Parts, and Chapters can all contain any lower level.

Narrative projects use one of several organizational patterns. Identify which one applies:

### 1. Flat Scene Structure

- **Location**: `/scenes/` directory with standalone scene files
- **Scene format**: `$i. $title.md` → `# Scene $i: $title` (e.g., `1. Opening Scene.md` → `# Scene 1: Opening Scene`)
- **Variable**: `$i` = numbers from 1+

### 2. Chapter-Based Structure

- **Location**: `/chapters/` directory with chapter folders (`$i. $title`)
- **Scenes within chapters**: Use `$ll. $title.md` with letter-based headers
  - **Format**: `a. Title.md` → `# Scene $i$ll: $title` (e.g., `# Scene 5a: Character Moment`)
  - **Variables**: `$i` = chapter number, `$ll` = lowercase letters (a, b, c)
- **Temporary scenes at root level**: Use `$ul. $title.md` 
  - **Format**: `A. Setup Scene.md` → `# Scene $ul: $title` (e.g., `# Scene A: Setup Scene`)
  - Stored at `/chapters/` root level, not in chapter folders

### 3. Part-Based Structure

- **Location**: `/parts/` directory with part folders (`$i. $title`)
- **When containing chapters**: Chapters (`$i. $title`) contain scenes in letter-based format (see Chapter-Based Structure)
  - Scenes use: `$ll. $title.md` → `# Scene $i$ll: $title`
- **When containing scenes directly**: Scenes use numbered format at part root level
  - Scenes use: `$i. $title.md` → `# Scene $i: $title` (follows Flat Scene Structure format)

### 4. Book-Based Structure

- **Location**: `/books/` directory with book folders (`$i. $title`)
- **When containing parts/chapters**: Parts or chapters contain scenes in letter-based format
  - Scenes use: `$ll. $title.md` → `# Scene $i$ll: $title` (where `$i` is chapter/part number)
- **When containing scenes directly**: Scenes use numbered format at book root level
  - Scenes use: `$i. $title.md` → `# Scene $i: $title` (follows Flat Scene Structure format)

### Scene Content Guidelines

- Scenes must have exactly ONE main heading matching the project's format
- Scene titles are typically 2-3 words (excluding "Scene", numbers, or articles)
- Scenes must NOT reference "the story" or other scenes directly
- Scenes must NOT have subheadings or section headers
- Scene title must align with actual scene content
- Keep character names, location names, and descriptions consistent

### Steps to Read Scenes
1. **Identify which structure exists** in the project root: `/scenes/`, `/chapters/`, `/books/`, or Part directories
2. **Navigate to the scene location** based on the structure type
3. **Read scene files** to understand:
   - Naming conventions and title format
   - Tone, style, and voice
   - Character names, personalities, and speech patterns
   - Geographic and setting details
   - Narrative flow and pacing
   - What has already happened in the story
4. **Read multiple scenes** to build understanding of character development, plot progression, and narrative patterns
5. **Note conventions** used in existing scenes (naming, formatting, narrative style, dialogue patterns)

## Characters (People)

Character information is stored in a `/people/` directory. Check if it exists.

### Person File Format
Each person file is typically JSON with structure:
- **id**: Identifier (e.g., `firstname_lastname`)
- **name**: Object with `given`, `middle`, `family`, `full`, `nickname`
- **description**: Brief character description
- **gender**: male/female/null
- **age**: Character's age (or null)
- **birthday**: Birth date (or null)
- **relationships**: Object containing:
  - **family**: `brothers`, `sisters`, `spouse`, `sons`, `daughters` (person IDs)
  - **friends**: Array of person IDs

### Steps to Get Character Context
1. **Check if `/people/` exists** in the project root
2. **If directory exists**:
   - Look for a TEMPLATE file to understand the standard format
   - Read ALL relevant people files for characters appearing in scenes you're working with
   - Understand each character's: age, personality, relationships, motivations, history, role in story
3. **If no `/people/` directory exists**:
   - Extract character info from existing scene content you've read
   - Track character names, descriptions, relationships, and background details across scenes
4. **Cross-reference** people files with scenes to understand how characters behave and interact
5. **Build character profiles** that include: personality traits, relationships, motivations, and development arc

## Locations

Location information may be stored in a `/locations/` directory. Check if it exists.

### Location File Format (JSON)

- **id**: Location identifier
- **name**: Location name
- **type**: Location type/category
- **description**: Detailed description
- **status**: Active or status description
- **areas**: Nested object structure with area/subarea definitions
  - Each area has: `id`, `name`, `type`, `description`, `positions`, `personnel`, `subareas`
- **primary_crew**: Array of person IDs
- **notable_events**: Array of events
- **personnel**: Array of person IDs
- **Additional fields**: May include vessel info, connected locations, etc.

### Location Directory Format (Markdown-Based)

- **Structure**: `location_name/` directory with `info.md` and subdirectories like `./rooms/`
- **info.md sections**:
  - Name
  - Description
  - Key Features
  - Areas/Rooms (reference to rooms/ subdirectory)
  - Characters (who lives/works there)
- **Subdirectories**: `./rooms/` or other area directories with individual markdown files that describe each room/area in detail

#### Room File Format
Each room markdown file typically contains:
- **Name**: Room/area name
- **Description**: Detailed description of the space, layout, and atmosphere
- **Key Features**: Distinctive elements, furnishings, or characteristics
- **Connected Areas**: Links to other rooms or areas
- **Notable Details**: Sensory details, history, or significance

### Steps to Get Location Context
1. **Check if `/locations/` exists** in the project root
2. **If directory exists**:
   - Look for TEMPLATE files to understand the standard format
   - Read location files (JSON or markdown) for locations featured in scenes
   - For markdown locations, read `info.md` and relevant room/area files
3. **If no `/locations/` directory exists**:
   - Extract location info from existing scene content you've read
   - Track location names, descriptions, geography, and sensory details across scenes
4. **Build location maps** that include: geography, layout, key features, and connected areas
5. **Understand location significance** in the narrative: which locations matter, who inhabit them, what events occur there
6. **Cross-reference location files with scenes ACTIVELY**:
   - Search for scenes that feature or describe the location
   - Read scenes where characters *access* or *describe* locations to verify details (entry points, geography, layout)
   - Watch for discrepancies between metadata and narrative descriptions
   - **Use logical/contextual reasoning**: Consider real-world plausibility (e.g., grocery store footprint, typical building structures, access patterns)
   - **Only treat scene descriptions as more accurate than metadata if a substantial amount of scenes consistently describe the location the same way differently from metadata**
   - A single or few scenes differing likely indicates an AI error in the scene, not metadata error
   - Metadata is the authoritative source unless there's a clear pattern across multiple scenes

7. **When you find a conflict between metadata and scenes**:
   - **If metadata is more logically sound** than contradicting scenes → Ask the user which is correct, then fix whichever they confirm is wrong (scenes or metadata)
   - **If scenes show a consistent pattern AND are more logically sound** than metadata → Update metadata and report to user
   - Always provide specific scene references when reporting inconsistencies to the user (e.g., "Scene 16a, Scene 17a")
   - Format: Describe the inconsistency, what changed, and why (including logical reasoning if applicable)
