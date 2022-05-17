# Wogrim-Misc-Unity
various scripts for doing things in unity

== to use ==
1. download zip
2. extract
3. put in your Unity project's Assets folder

scripts may not work in different versions of Unity

## DeleteExtraBones
created for modding Koikatsu clothes to delete body bones (GameObjects) that the clothes don't use (from imported clothes FBX)

needs enimaroah's BlenderFBX_Postprocessor script to remove references to unused bones from any Skinned Mesh Renderers

== to use ==
1. drag FBX into scene
2. put this script on root GameObject
3. extra bones will be automatically deleted and the script will remove itself
4. continue making item as usual

extra bones are defined as:
- bone is not used by any Skinned Mesh Renderer
- bone does not have any components besides transform
- bone does not have any child bones that can't be deleted

## CreateAssetBundles
created to build asset bundles for modding Koikatsu; builds with LZ4 compression for Windows 64-bit

not needed in KK Modding Tools because it has a much more robust set of scripts for building asset bundles

== to use ==
1. assign textures, prefabs to asset bundles (in the bottom of Inspector window)
2. click new menu button: Assets -> Build Asset Bundles
3. creates asset bundles in Assets/_Asset Bundles
4. copy asset bundle(s) to separate folder (outside of Unity) and make your mod

if it doesn't seem to be detecting that the asset bundle should be rebuilt, delete the whole "_Asset Bundles" folder and try again
