---
layout: post
title: Disable expand file content in Visual Studio Solution Explorer
---

I don't like the expand file content feature in Visual Studio Solution Explorer as I think it clutters the ui and I never use it.
Fortunatelly there is a way to disable it.

1. Open regedit.
2. Go to **HKEY_CURRENT_USER\Software\Microsoft\VisualStudio\{version}**.
3. Add a new dword value named **UseSolutionNavigatorGraphProvider** with a value of **0**.
4. Restart Visual Studio
5. Enjoy =)