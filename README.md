# EasyApp.ConsoleApp 
## A MonoGame inspired console app library

EasyApp.ConsoleApp is meant to make more interactive, frame-rate independent
console apps easier to make. It does this through the same syntactic structure that MonoGame (https://monogame.net/) also provides.  

## An Example How-To:

Firstly:
```sh
using EasyApp.ConsoleApp.net8;
```

You can simply create your custom console app implementation like this:

```sh
//Inherit from EasyConsoleApp, you can also limit the frames per second.
public class App : EasyConsoleApp
{
    public App() : base(fps: 30)
    {

    }

    protected override void Initialize()
    {
        //Write your own Initialize logic...
    }

    protected override void ProcessInput()
    {
        //Can be a switch statement with conditions revolving around simple keys.
    }

    protected override void Update()
    {
        //A simple update method.
    }

    protected override void Render()
    {
        //I normally just update an array of strings and draw each element.
    }
}


```
Running the custom app implementation:
```sh
var app = new App();
app.Run();
```

Not to bad, right? 


## License

MIT

