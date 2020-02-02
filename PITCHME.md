---?image=assets/img/swetugg_butterfly_text_bw.png&size=50% auto&position=50px 50px&opacity=50
@title[Azure DevOps Pipelines as code using C#]
Azure DevOps Pipelines
</br>
as code using C# @fa[rocket text-orange]

@snap[south-east text-08]
@fa[twitter] @fa[medium] @fa[github] <a style='text-decoration: none; color: white;' href='https://twitter.com/devlead'>@devlead</a> - Mattias Karlsson
@snapend
---
@title[Setting the stage]
@snap[west]
# @fa[bullhorn text-gray] 
@snapend

@snap[east span-83]
@ul[none]
- @fa[retweet] Improved DevOps feedback loop
- @fa[recycle] Reuse patterns you know
- @fa[yin-yang] Consistent experience
- @fa[smile] Joyful experience
@ulend
@snapend

---
@title[Mattias Karlsson]
@snap[east]
# @fa[user text-gray] 
@snapend

@snap[west span-83]
@ul[none]
- @fa[briefcase] Partner & Sr. architect at WCOM @note[a Microsoft partner located in Gothenburg, Sweden.]
- @fa[cloud] Microsoft Azure MVP @note[Head in the cloud.]
- @fa[wrench] Microsoft Developer Technologies MVP @note[Still gets my hands dirty.]
- @fa[magic] OzCode Magician community @note[Passion for diagnosing and fixing broken code]
- @fa[code-fork] Open source  @note[Active in the open source community. Most know there for being one of the maintainers behind the Cake build system, which is now also part of the .NET foundation.].
- @emoji[family] Husband of 1, father of 2 @note[last but not least]
@ulend
@snapend
---
@title[Azure DevOps Pipelines Classic/YAML]
@snap[north span-100]
## @fa[rocket]
@snapend

@snap[north-west span-48 fragment]
## Classic
@ul[none]
- @fa[check] Low barrier to entry
- @fa[check] Intuitive
- @fa[times] Hard to maintain
- @fa[times] Unicorn
@ulend
@snapend

@snap[north-east span-48 fragment]
## YAML
@ul[none]
- @fa[check] More maintainable @note[Versions with code.]
- @fa[check] Easier reuse
- @fa[times] Discoverbility
- @fa[times] High barrier to entry
@ulend
@snapend
---
@title[Azure DevOps Pipelines Feedback loop]
@snap[north span-100]
## @fa[retweet]
@snapend

@snap[midpoint span-54]
@ul[none]
- @fa[edit] Edit
- @fa[save] Save
- @fa[play] Run / Commit&Push @fa[cloud-upload-alt]
- @fa[hourglass-start] Wait
- @fa[coffee] @fa[hourglass-half]
- @fa[redo]
@ulend
@snapend
---
@title[Cake Improved Experience & Feedback loop]
@snap[north span-4]
@img[borderless](/assets/img/cake.svg)
@snapend

@snap[north-west span-48 fragment]
## Experience
@ul[none]
- @fa[check] Discoverable
- @fa[check] Reusable
- @fa[check] Maintainable
@ulend
@snapend

@snap[north-east span-48 fragment]
## Workflow
@ul[none]
- @fa[edit] Edit
- @fa[save] Save
- @fa[play] Run @fa[home] @fa[redo]
- @fa[cloud-upload-alt] Commit&Push
- @fa[hourglass-start] Wait
- @fa[coffee] @fa[hourglass-half] @fa[redo]
@ulend
@snapend
---
@title[Cake?]

@snap[west span-24]
@img[borderless](/assets/img/cake.svg)
@snapend

@snap[east span-60]
@ul[none]
- @fa[random] Cross platform @note[Mac, Windows, Linux]
- @fa[random] Cross environment @note[Local, OnPrem, Cloud, Container]
- @fa[random] Cross service @note[Azure DevOps, GitHub Actions, AppVeyor, 
- @fa[random] Cross runtime @note[.NET Core, .NET Framework, Mono]TeamCity, Bitbucket, Travis, etc.]
- @fa[code-branch] Open source
- @fa[tools] Build orchestration tool
- @fa[file-alt] C# DSL
@ulend
@snapend
---
@title[Common pipeline]

@snap[north text-center]
@ul[process]
- @fa[cloud-download] Restore @note[Restore dependencies from i.e. NuGet]
- !
- @fa[cogs] Build
- !
- @fa[flask] Test
- !
- @fa[archive] Package
- !
- @fa[cloud-upload] Publish @note[Publish artifacts to i.e. NuGet]
@ulend
@snapend
---
@title[Restore]

@snap[north]
@fa[cloud-download] Restore
@snapend

@snap[north-west span-60 fragment]
## Classic
@img[borderless fragment](assets/img/adoclassic/restore.png)
@snapend

@snap[north-east span-60 fragment]
## YAML
@code[yaml fragment](assets/yaml/restore.yaml)
@snapend

@snap[south-east span-60 fragment]
## CAKE
@code[csharp fragment](assets/cake/restore.cake)
@snapend
---
@title[Build]

@snap[north]
@fa[cogs] Build
@snapend

@snap[north-west span-60 fragment]
## Classic
@img[borderless fragment](assets/img/adoclassic/build.png)
@snapend

@snap[north-east span-60 fragment]
## YAML
@code[yaml fragment](assets/yaml/build.yaml)
@snapend

@snap[south-east span-60 fragment]
## CAKE
@code[csharp fragment](assets/cake/build.cake)
@snapend
---
@title[Test]

@snap[north]
@fa[flask] Test
@snapend

@snap[north-west span-60 fragment]
## Classic
@img[borderless fragment](assets/img/adoclassic/test.png)
@snapend

@snap[north-east span-60 fragment]
## YAML
@code[yaml fragment](assets/yaml/test.yaml)
@snapend

@snap[south-east span-60 fragment]
## CAKE
@code[csharp fragment](assets/cake/test.cake)
@snapend
---
@title[Package]

@snap[north]
@fa[archive] Package
@snapend

@snap[north-west span-30 fragment]
## Classic
@img[borderless fragment](assets/img/adoclassic/package.png)
@snapend

@snap[north-east span-70 fragment]
## YAML
@code[yaml fragment](assets/yaml/package.yaml)
@snapend

@snap[south-east span-70 fragment]
## CAKE
@code[csharp fragment](assets/cake/package.cake)
@snapend