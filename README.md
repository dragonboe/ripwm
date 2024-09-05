# ripwm
🪐 [ Rip Window Manager ] Minimal / Fast

- Written with C and Windows API and utilizes existing Windows facilities, resulting in very slim code.

## How to use

- After building, run the executable `ripwm.exe` which will reside in the release and/or debug folder, depending on what you built.

NOTE : Upon running, it will immediately tile all the non-minimized windows on your screen.

The program will run in the background. To quit ripwm, use ```alt+q```.

You can use ```alt+j``` and ```alt+k``` to go to the next/previous window with your keyboard.

You can use ```alt+f``` hotkey to toggle fullscreen mode which will disable tiling and put the focused window in fullscreen, pressing ```alt+f``` again will enable tiling again and tile all non-minimized windows

You can use ```alt+1``` up until ```alt+9``` to go to workspace number ```1``` until ```9``` respectively

You can move the current focused window to a different workspace number by adding ```shift``` to the above command.

## Building

You can build using the "x64 Native Tools Command Prompt for VS 2022" that comes with Microsoft Visual Studio Build Tools:

In the console you can run nmake to build according to the Makefile

```nmake```

I haven't tried building with a different VS version or building x86, but that may work as well.

## Contributing

You can change or edit.

## Coding Conventions

#### Spacing

Tabs > Spaces

#### Function and variable names

Functions and variables should be in camelCase

#### Comments

In general comments should be avoided unless they are absolutely necessary

Avoid adding obvious comments on the code like:
```c
// Prints hello on the screen
printf("Hello!\n");
```

Avoid comments explaining the logic in other words:
```c
// Allocate memory for the string and for the null terminator
malloc(1024 + 1);
```

Instead something like this is much better:
```c
const int nullTermSize = 1;
malloc(strlen(path) + nullTermSize);
```

Example of when a comment is necessary and has added value:
```c
// This DLL is loaded into many processes on the computer, therefore we need to keep the logic here as simple as possible to avoid slowing down the system
```

#### Pointers

```int*``` and not ```int *```

#### for/while/switch/if blocks

Opening braces ```{``` in the same line as the block definition

```c
if (cond) {
}
```

and not:

```c
if (cond)
{
}
```

Space between the block name and the brackets

```if (statement)``` and not ```if(statement)```

#### Function blocks

Opening braces ```{``` in a new line after the function definition

```c
void init()
{
}
```

and not:

```c
void init() {
}
```
