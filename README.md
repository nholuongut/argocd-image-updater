# Argo CD Image Updater

![](https://i.imgur.com/waxVImv.png)
### [View all Roadmaps](https://github.com/nholuongut/all-roadmaps) &nbsp;&middot;&nbsp; [Best Practices](https://github.com/nholuongut/all-roadmaps/blob/main/public/best-practices/) &nbsp;&middot;&nbsp; [Questions](https://www.linkedin.com/in/nholuong/)
<br/>

## Introduction

Argo CD Image Updater is a tool to automatically update the container
images of Kubernetes workloads which are managed by Argo CD. In a nutshell,
it will track image versions specified by annotations on the Argo CD
Application resources and update them by setting parameter overrides using
the Argo CD API.

Currently it will only work with applications that are built using *Kustomize*
or *Helm* tooling. Applications built from plain YAML or custom tools are not
supported yet (and maybe never will). 

## Current status

Argo CD Image Updater is under active development. We would not recommend it
yet for *critical* production workloads, but feel free to give it a spin.

We're very interested in feedback on usability and the user experience as well
as in bug discoveries and enhancement requests.

**Important note:** Until the first stable version (i.e. `v1.0`) is released,
breaking changes between the releases must be expected. We will do our best
to indicate all breaking changes (and how to un-break them) in the
[Changelog](CHANGELOG.md)

## Contributing

You are welcome to contribute to this project by means of raising issues for
bugs, sending & discussing enhancement ideas or by contributing code via pull
requests.

In any case, please be sure that you have read & understood the currently known
design limitations before raising issues.

Also, if you want to contribute code, please make sure that your code

* has its functionality covered by unit tests (coverage goal is 80%),
* is correctly linted,
* is well commented,
* and last but not least is compatible with our license and CLA

Please note that in the current early phase of development, the code base is
a fast moving target and lots of refactoring will happen constantly.

## License

`argocd-image-updater` is open source software, released under the
[Apache 2.0 license](https://www.apache.org/licenses/LICENSE-2.0)

## Things that are planned (roadmap)

The following things are on the roadmap until the `v1.0` release

* [ ] Extend Argo CD functionality to be able to update images for other types
  of applications.

* [x] Extend Argo CD functionality to write back to Git

* [ ] Provide web hook support to trigger update check for a given image

* [x] Use concurrency for updating multiple applications at once

* [x] Improve error handling

* [x] Support for image tags with i.e. Git commit SHAs

For more details, check out the
[v1.0.0 milestone](https://github.com/nholuongut/argocd-image-updater/milestone/1)

## Frequently asked questions

**Does it write back the changes to Git?**

We're happy to announce that as of `v0.9.0` and Argo CD `v1.9.0`, Argo CD
Image Updater is able to commit changes to Git. It will not modify your
application's manifests, but instead writes
[Parameter Overrides](https://github.com/nholuongut/argo-cd/parameters/#store-overrides-in-git)
to the repository.

We think that this is a good compromise between functionality (have everything
in Git) and ease-of-use (minimize conflicts).

**Are there plans to extend functionality beyond Kustomize or Helm?**

Not yet, since we are dependent upon what functionality Argo CD provides for
these types of applications.

**Will it ever be fully integrated with Argo CD?**

In the current form, probably not. If there is community demand for it, let's
see how we can make this happen.

There is [an open proposal](https://github.com/argoproj/argo-cd/issues/7385) to migrate this project into the `argoproj` org (out
of the `nholuongut` org) and include it in the installation of Argo CD.

# 🚀 I'm are always open to your feedback.  Please contact as bellow information:
### [Contact ]
* [Name: Nho Luong]
* [Skype](luongutnho_skype)
* [Github](https://github.com/nholuongut/)
* [Linkedin](https://www.linkedin.com/in/nholuong/)
* [Email Address](luongutnho@hotmail.com)
* [PayPal.me](https://www.paypal.com/paypalme/nholuongut)

![](https://i.imgur.com/waxVImv.png)
![](Donate.png)
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/nholuong)

# License
* Nho Luong (c). All Rights Reserved.🌟
