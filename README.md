# MergeTest
Dummy Repo for Testing Ue4 Merging of Binary Uasset Files

Goal is to determine the feasibility of merging uasset files using the in-editor merge tool. Comparing it to the equivalent workflow commonly done with a text editor, like Visual Studio, for text files.

Thus far, it seems that only Blueprints and Animation Blueprints have a functional editor merge tool. These types would correspond with the following file prefixes:

BP_ Genral Blueprint Classes that inherit from AActor
ABP_ The specialized Blueprint asset for storing animation graphs and bound state machines
GM_ Blueprint Class that inherits from either UGameMode or UGameModeBase
GI_ Blueprint Class that inherits from UGameInstance
PC_ Blueprint Class that inherits from UPlayerController
AIC_ Blueprint Class that inherits from UAIController

Other assets may work too, but only if they are created through one of the following methods in the editor:
1. Right-Click in Content Browser -> Create Basic Asset -> Blueprint Class OR
2. Right-Click in Content Browser -> Create Advanced Asset -> Animation -> Animation Blueprint

Recommendation: Make and exception, based on the above file prefixes, for .uasset files that can be merged with the editor tool provided by the engine standard vanilla Git plugin.
