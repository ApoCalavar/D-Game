# D-Game
D-Game Is a Game Developing tool that Uses the D Programing Language.
Scriped in C#.
Tutorials:
1=Window:
module [Reaplese With Your Defalt Module];

import core.sys.windows.windows;

alias extern(C) int function(string[] args) MainFunc;
extern (C) int _d_run_main(int argc, char **argv, MainFunc mainFunc);

extern (Windows)
int WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
{
    return _d_run_main(0, null, &main); // arguments unused, retrieved via CommandLineToArgvW
}

extern(C) int main(string[] args)
{
    MessageBoxW(null, "(Window Text)"w.ptr, "(Window Title)"w.ptr, MB_OK);
    return 0;
}
