# DemonLord Energy — Master Planning Document

## Project summary
DemonLord Energy — a cinematic 3D product site showcasing 10 ultra-detailed cans (angelic, demonic, cosmic). Each can opens a fullscreen 3D viewer with 360° rotation, zoom, and theme-appropriate environment lighting. The site is optimized for web (GLB/GLTF models, Draco compression, progressive loading).

## Goals
- Deliver a working frontend that loads 10 GLB cans, each opening a themed 3D scene.
- Provide production-ready prompts and instructions for creating high-quality GLB assets.
- Ensure fast load times using DRACO compression and texture optimization.
- Provide a fallback procedural viewer so site is demoable without GLBs.

## Core features (MVP)
1. Landing gallery of 10 cans (thumbnails + meta).  
2. Fullscreen 3D viewer per can with OrbitControls (360°), zoom, auto-rotate.  
3. Theme environments: Angelic (soft god-rays, feathers), Demonic (embers, lava), Cosmic (nebula, star dust).  
4. Material support: PBR maps (albedo, normal, roughness, metalness, emissive).  
5. Fallback procedural can if GLB missing.  
6. Responsive UI and accessible keyboard controls (Esc closes viewer, arrows rotate).

## Flavor list (10)
**Angelic**: Divine Light, Seraphic Dawn, Gracefall Peach  
**Demonic**: Blood Moon, Hellforge Ember, Abyssal Wail, Infernal Zero  
**Cosmic**: Nebula Ascension, Voidbreaker, Celestial Rift

## Asset & model requirements
- GLB per can: single scene, centered at origin, Y-up.  
- PBR textures: albedo (PNG/JPEG), normal (PNG), roughness+metalness (combined or separate), emissive if needed.  
- Recommended max texture: 2048 → downscale to 1024 for web build.  
- Optional: Draco compression for GLB.

## Prompts (example snippets for 3D artist / AI model)
**Blood Moon (GLB prompt)**:
"Photorealistic aluminum can GLB: matte black base, embossed demonic relief, sculpted demon face crown, engraved runes with subtle emissive veins (red), high resolution normal map, PBR textures, studio HDRI lighting. Deliver glb with albedo, normal, roughness, emissive. Optimize and use Draco."

(Repeat/adjust per flavor with angelic/cosmic variants.)

## Tech stack
- Frontend: plain HTML/CSS/JS + Three.js (GLTFLoader, OrbitControls).  
- Build: static site (GitHub Pages / Vercel / Netlify).  
- Tools: Blender for modeling, gltf-transform / gltf-pipeline for compression.

## Folder structure (recommended)
