# Hare

<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![License][license-shield]][license-url]


<!-- TABLE OF CONTENTS -->
## Table of Contents

- [Hare](#hare)
  - [Table of Contents](#table-of-contents)
  - [Getting Started](#getting-started)
    - [Prerequisites](#prerequisites)
    - [Installation](#installation)
  - [Usage](#usage)
  - [License](#license)

<!-- GETTING STARTED -->
## Getting Started

To get a local copy up and running follow these simple steps.

### Prerequisites

Make sure you have Rust installed. 

```shell
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

Rocket uses the nightly version of Rust so make sure you use that. If you'd like to only use nightly for this project, you can run this from the root of the project after cloning.

```sh
# from the root of the project
rustup override set nightly
```

### Installation
 
1. Clone the project
```sh
git clone https://github.com/jkjetty/hare.git
```
2. Make sure you're using nightly 
```sh
cargo --version
```
3. Build the project
```sh
cargo build
```
4. Run the project
```sh
cargo run
```
5. Visit [localhost:8000](http://localhost:8000/)
6. To test a command, go to [localhost:8000/search?cmd=tw](http://localhost:8000/search?cmd=tw) and you should be redirected to Twitter

<!-- USAGE EXAMPLES -->
## Usage

To test out a command, type in http://localhost:8000/search?cmd= followed by your command.

See supported commands in the [`redirect_url` list](https://github.com/jkjetty/hare/blob/master/src/main.rs).

Everything else redirects to a google search with your query. 

<!-- Default search -->
## Setting Hare as your default search engine

Chrome instructions:
- Go to `chrome://settings`
- Click the "Search engine" tab on the right
- Click "manage search engines"
- Under "Site search" click the "Add" button
- Enter "hare" for the search engine and shortcut
- Enter `localhost:8000/search?cmd=%s` as the URL 
- Click "Add" to save the search engine
- Click the menu (three dots) next to your new entry
- Click "Make default" 
- Open a new tab and try it out! Enter "g robot vacuums" and make sure google search comes up

<!-- LICENSE -->
## License

Distributed under the MIT License. See [`LICENSE`](LICENSE) for more information.

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/after-ephemera/hare.svg?style=flat-square
[contributors-url]: https://github.com/after-ephemera/hare/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/after-ephemera/hare.svg?style=flat-square
[forks-url]: https://github.com/after-ephemera/hare/network/members
[stars-shield]: https://img.shields.io/github/stars/after-ephemera/hare.svg?style=flat-square
[stars-url]: https://github.com/after-ephemera/hare/stargazers
[issues-shield]: https://img.shields.io/github/issues/after-ephemera/hare.svg?style=flat-square
[issues-url]: https://github.com/after-ephemera/hare/issues
[license-shield]: https://img.shields.io/github/license/after-ephemera/hare?style=flat-square
[license-url]: https://github.com/after-ephemera/hare/blob/master/LICENSE
[product-screenshot]: demo.gif
