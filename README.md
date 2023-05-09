<!-- Project shields -->
<div align="center">
  <a href="https://www.nodejs.org/">
    <img src="https://img.shields.io/badge/node-v19.9.0-informational?style=flat-square">
  </a>
  <a href="https://www.vuejs.org/">
    <img src="https://img.shields.io/badge/vue-v3.2.47-informational?style=flat-square">
  </a>
</div>

<!-- Project title -->
<div align="center">
  <h3>Data and clouds - Web app</h3>
  <p>A web app for the data and clouds management course.</p>
</div>

<!-- Table of contents -->
<details>
  <summary>Table of contents</summary>
  <ol>
    <li><a href="#about">About</a></li>
    <li>
      <a href="#getting-started">Getting started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li>
      <a href="#usage">Usage</a>
      <ul>
        <li><a href="#run-the-development-server">Run the development server</a></li>
        <li><a href="#build-the-project">Build the project</a></li>
      </ul>
    </li>
  </ol>
</details>

## About

This web app is made during the data and clouds management course.
The point of this project is to deploy a web app on Microsoft Azure that provide a custom interface to the Stable Diffusion model.

## Getting Started

### Prerequisites

To run the application on a machine, some prerequisites are needed.

* [Node.js](https://www.nodejs.org/)

### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/peticle/petignat-fluck-data-clouds-frontend.git
   ```
2. Install the dependencies using npm
   ```sh
   cd petignat-fluck-data-clouds-frontend
   npm install
   ```

## Usage

### Run the development server

```sh
# Run the devlopment server
npm run dev

# Access the URL in a browser
firefox http://localhost:5173/
```

### Build the project

```sh
# Build the project
npm run build
```

