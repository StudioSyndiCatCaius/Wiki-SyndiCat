## Noireamore Academy - FAQ


___
#### Q. My game is crashing on startup. How do I ix it?

A. The most common reason this happens is due to an incompatible graphics card with the game's default renderer (**Direct X 12**).

To Fix (Windows):
* Open windows explorer to "%LOCALAPPDATA%\NoiramoreAcademy\Saved\Config\Windows"
* Open "*GameUserSettings.ini*" and find or add the field ``DefaultGraphicsRHI`` under the category ``[/Script/WindowsTargetPlatform.WindowsTargetSettings]``.
* set the field to your desired graphics renderer. If DX12 is giving you issues, try DX11.
    * *DirectX 11* = ``DefaultGraphicsRHI_DX11``
    * *DirectX 12* = ``DefaultGraphicsRHI_DX12``
    * *Vulkan* = ``DefaultGraphicsRHI_Vulkan``
* It should not look something like this:
````ini
[/Script/WindowsTargetPlatform.WindowsTargetSettings]
DefaultGraphicsRHI=DefaultGraphicsRHI_DX11 
````
* Save "*GameUserSettings.ini*" and restart the game.