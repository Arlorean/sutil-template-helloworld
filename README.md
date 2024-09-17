## Sutil Template for Hello World

The simplest Sutil application showing how a single page application is constructed and mounted with minimal styling. See:
- [src/App/App.fs](src/App/App.fs)
- [public/index.html](public/index.html)

```fs
module App

open Sutil
open Sutil.DOM
open Sutil.Attr

let view() =
    Html.div [
        style [
            Css.fontFamily "Arial, Helvetica,sans-serif"
            Css.textAlign "center"
            Css.marginTop "40px"
            Css.fontSize "10ex"
        ]
        text "Hello World"
    ]

mountElement "sutil-app" (view())
```

### Quick Start

- Install [Prerequisites](#prerequisites)
- Download [Template](#template)
- Restore [Dependencies](#dependencies)

```
    cd sutil-template-helloworld
    npm install
    npm run start
```

### Prerequisites

- [.NET Core SDK](https://dotnet.microsoft.com/) to work with F# files and dependencies [.NET 6.0.300](https://dotnet.microsoft.com/en-us/download/dotnet/6.0)
- [Node.js](https://nodejs.org/) to execute JavaScript code and manage npm packages (includes [npm](https://www.npmjs.com/)) 

### Template
 - Download and unzip [main.zip](https://github.com/davedawkins/sutil-template-helloworld/archive/refs/heads/main.zip)
 - OR [install git](https://git-scm.com/) and run
   ```
   git clone -s https://github.com/davedawkins/sutil-template-helloworld.git
   ```

### Dependencies

Run the command to install the dependencies:
- [Sutil](https://www.nuget.org/packages/Sutil) nuget package
- [Paket](https://www.nuget.org/packages/Paket) package manager
- [Fable](https://fable.io/) F# to JavaScript compile and runtime 

```
    cd sutil-template-helloworld
    dotnet tool restore

    cd /src/App
    dotnet restore
```

### What Next

It's recommended that for any kind of "real" app that you adopt the Elmish MVU pattern.  
Template: https://github.com/davedawkins/sutil-template-elmish
