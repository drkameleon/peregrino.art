<p align="center"><img width="90%" align="center" src="https://raw.githubusercontent.com/drkameleon/peregrino.art/master/logo.png"/></p>
<p align="center">
     Lightning-fast command-line<br>benchmarking tool & library for Arturo
     <br><br>
     <img src="https://img.shields.io/github/license/arturo-lang/grafito?style=for-the-badge">
    <img src="https://img.shields.io/badge/language-Arturo-orange.svg?style=for-the-badge">
</p>


<p align="center"><img width="90%" align="center" src="https://raw.githubusercontent.com/drkameleon/peregrino.art/master/peregrino.gif"/></p>

--- 
 
<!--ts-->

* [What does this package do?](#what-does-this-package-do)
* [How do I use it?](#how-do-i-use-it)
   - [As a library](#as-a-library)
   - [From the terminal](#from-the-terminal)
* [License](#license)   

<!--te-->
 
---

### What does this package do?

This is a benchmarker tool to help you measure and compare different scripts, in an ultra-customizeable way, see the results in an intuitive way and... even export them (Json & Markdown supported so far!) in case you want to keep them for further processing.

> [!NOTE]
> Peregrino has shamelessly been inspired by a tool I personally love: [Hyperfine](https://github.com/sharkdp/hyperfine). See it mostly as a double personal challenge: a) see how easily this could be done in Arturo, using what we already have, and... b) make something even better and more user-friendly!

### How do I use it?

Peregrino comes in a *hybrid* package; that is: you may use it as a library (via `import`), or you can actually run it via the command-line, after installing it.

#### As a library

```red
import {peregrino}!

P: to :peregrino @["command one", "command two"]!
P\benchmark ; and that's it!
```

#### From the terminal

When properly installed, you should be able to run Peregrino as any normal command, directly from your terminal.

A brief preview of all the options (identical to the output of `--help`):

```
Usage:
    peregrino [options] <command>,...

Arguments:
    <command>
        One or more commands you want to benchmark

Options:
    -r, --run <times>           Specify number of times to run each command 
    -f, --file                  Read commands from text file (one per line) 
    -p, --params <string>       Use custom params in command 

    -m, --minimal               No fancy output; just the data! 
    -a, --ascii                 Use simple style, with ASCII-only characters 
    -c, --colorless             Don't use colored output 

        --markdown <file>       Export Markdown to given file 
        --json <file>           Export Json to give file 

    -h, --help                  Show this help screen 
    -v, --version               Print version 
```

> [!IMPORTANT]
> Arturo - and thus Peregrino - use the Nim-inspired way of parsing command-line params. Thus, for setting the `--run` param, you should use `:` before the value, e.g.:
> ```
> peregrino --run:10 "some command" "another command" ...
> ```

<hr/>

### License

MIT License

Copyright (c) 2024 Yanis Zafirópulos

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
