# Interactive Vector Field Visualizations and Presentations

This repository contains a small collection of interactive demonstrations and presentation decks that explore vector addition and vector fields in both two and three dimensions. The demos are written in vanilla HTML, CSS and JavaScript (with the help of [three.js](https://threejs.org) for the 3‑D scenes) and are intended for educational use. Two PowerPoint presentations are also provided in Base64 form so they can be stored as plain text within this repository.

## Contents

| File | Description |
| --- | --- |
| **`2D.html`** | A simple interactive demo that visualizes 2‑D vector addition. Drag the arrow endpoints to see how vectors add head‑to‑tail and how the resultant vector changes. |
| **`2D Field.html`** | A 2‑D vector field particle visualization. The code animates particles moving through a user‑defined vector field, giving insight into field behaviour. |
| **`3D.html`** | A 3‑D vector addition demo where you can drag points in space and watch the resultant vector update in real time. This example uses three.js to render the scene. |
| **`3D Field.html`** | A 3‑D vector field particle visualizer. Particles are advected through a 3‑D vector field; controls allow you to tweak field parameters and observe how trajectories change. |
| **`Vector_Fields_in_Multivariable_Calculus_pptx.b64`** | Base64 encoded PowerPoint deck for the English presentation titled *“Vector Fields in Multivariable Calculus”*. Decode this file to recover the original `.pptx` (see below). |
| **`Vector_Fields_CN_pptx.b64`** | Base64 encoded PowerPoint deck for the Chinese presentation. Decode this file to recover the Chinese version of the slides. |

## How to Use

### Running the HTML demos

You can also view each demo online via GitHub Pages:

- [2D demo](https://yinl-k.github.io/vector-fields-project/2D.html)
- [2D field demo](https://yinl-k.github.io/vector-fields-project/2D%20Field.html)
- [3D demo](https://yinl-k.github.io/vector-fields-project/3D.html)
- [3D field demo](https://yinl-k.github.io/vector-fields-project/3D%20Field.html)

The HTML files can be opened directly in a browser. However, browsers sometimes restrict local file access, which may prevent the demos from loading external modules (such as three.js) when opened via a `file:///` URL. To avoid this, you can serve the files via a local web server:

```
# Install a simple static file server (if you don't already have one)
npm install -g http-server

# From the repository root, start the server on port 8080
http-server -p 8080

# Now open a browser and navigate to
# http://localhost:8080/2D.html
# http://localhost:8080/2D%20Field.html
# http://localhost:8080/3D.html
# http://localhost:8080/3D%20Field.html
```

Interacting with the demos is straightforward: click and drag on the arrows or particles to explore vector addition and flow dynamics. Each page includes on‑screen controls and explanatory text.

### Decoding the PowerPoint files

The PowerPoint presentations are stored as Base64‑encoded text files to keep them versionable in Git. To restore the original `.pptx` files, decode the Base64 and write the output to a file:

```
# Decode the English presentation
awk '{ printf "%s", $0 }' Vector_Fields_in_Multivariable_Calculus_pptx.b64 | base64 -d > "Vector Fields in Multivariable Calculus.pptx"

# Decode the Chinese presentation
awk '{ printf "%s", $0 }' Vector_Fields_CN_pptx.b64 | base64 -d > "向量场与多变量微积分.pptx"
```

On Windows, you can use a tool like PowerShell or an online Base64 decoder; just ensure the entire contents of the `.b64` file are decoded without line breaks.

## License

These demos and presentations are provided for educational purposes. You are free to use and modify the code for non‑commercial teaching or personal study. If you build upon or redistribute this material, please credit the original author.
