# SafeGuiTester
A very small library for testing applications using my Gui library safely

# Archived
This repository is archived because the Gui repository itself is also archived.

# Description
This library only consists of a single class with a single public method start. In order to use this library, you need to have jnativehook,
Gui (and eventually GLGui and LWJGL if that's what you want to test) and your own gui application on your buildpath.

To use this library, you need to create an instance of GuiWindow. Just the instance you use when you use your application. Then you need
to set the main component of the window by calling its setMainComponent method. Do NOT call the open or run method of the window, that
will be done by the test. Also, you need to create a class that implements GuiTestProgram, that will be your test.

Once you have that, call SafeGuiTester.testSafely(test, window). If you want to terminate the test, press the x-button on your keyboard.

This is not part of the Gui library itself because this requires jnativehook.
