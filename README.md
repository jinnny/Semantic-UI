
publishing-style-guide
=======================

골자는 semantic UI를 쓰되, 불필요한 부분은 제거한 소스입니다.
기본은 test 에 있는 형태로 사용하며, 프로젝트에 따라, 컬러, 모양 등은 따로 커스텀해서 사용합니다.


커스텀 내용
--------------------------

1. 모든 태그에 font-family 제거 (다국어 대체를 위해 _fonts.scss를 쓰기 위함)
2. margin 값 제거 (h1-h6, p)
3. 테두리 라운드 0 처리 (border-radius: 0)
4. b, strong 폰트 두께 상속값으로 변경 (font-weight: inherit)
5. body 태그의 background, min-width 값 제거
6. dropdown .text:not(.default)쪽 불필요한 두께/색 제거
7. dropdown(modules)의 min-width, min-height 값 제거
8. input의 안쪽 shadow 제거 (ios 문제, -webkit-appearance: inherit)
9. mark 태그의 배경색 투명하게 변경, 폰트색 상속값으로 변경
10. 아이콘 폰트 및 이미지 경로 변경 (assets 폴더에 함께 움직이기 위함)


style 구조
----------
> base/
>> _reset.scss  (초기화)  <br>
>> _fonts.scss  (폰트)<br> 

> components/ (버튼, 모달 등 위젯, 컴포넌트)
>> _buttons.scss (버튼)<br>
>> _modal.scss (모달)<br>
>> …             (기타)

>layout/  (사이트의 주요 레이아웃 )<br>
>>_header.scss      (헤더)<br>
>>_footer.scss      (푸터)<br>
>>_common.scss   (레이아웃 공통요소)<br>
>> …                    (기타)

> pages/ (각페이지)
>> _index.scss   (메인)<br>
>> …             (기타)

> utils/ (프로젝트에서 사용되는 모든 Sass 도구와 헬퍼)

>>_var.scss   (변수)<br>
>>_mixins.scss      (믹스인)

> vendor/ (외부 라이브러리와 프레임워크)
>> _semantic.css

>–index.scss(index.css)  메인 파일) 

구조 네이밍 규칙
----------------
1. 임포트 될 파일은 파일명 앞에 언더바(_)를 사용해야합니다. ex) _main.scss
1. 단어와 단어사이는 하이픈(-)을 사용해야합니다. ex) _main-content.scss


![Semantic](http://semantic-ui.com/images/logo.png)

# Semantic UI

[![Join the chat at https://gitter.im/Semantic-Org/Semantic-UI](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/Semantic-Org/Semantic-UI?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

[![CDNJS](https://img.shields.io/cdnjs/v/semantic-ui.svg)](https://cdnjs.com/libraries/semantic-ui/)

[Semantic](http://www.semantic-ui.com) is a UI framework designed for theming.

Key Features
* 50+ UI elements
* 3000 + CSS variables
* 3 Levels of variable inheritance (similar to SublimeText)
* Built with EM values for responsive design
* Flexbox friendly

Semantic allows developers to build beautiful websites fast, with **concise HTML**, **intuitive javascript**, and **simplified debugging**, helping make front-end development a delightful experience. Semantic is responsively designed allowing your website to scale on multiple devices. Semantic is production ready and partnered with frameworks such as **React**, **Angular**, **Meteor**, and **Ember**, which means you can integrate it with any of these frameworks to organize your UI layer alongside your application logic.

## 2.4.0 Release (Sep 17th, 2018)

Semantic UI `2.4` is now available. Read up on [what's new](http://www.semantic-ui.com/introduction/new.html) in the docs.

Migration info from `1.x` can be found in the [2.0 release notes](https://github.com/Semantic-Org/Semantic-UI/blob/master/RELEASE-NOTES.md#version-200---march-xx-2015)

## User Support

Please help us keep the issue tracker organized. For technical questions that do not include a specific [JSFiddle test case](https://jsfiddle.net/ca0rovs3/) (bug reports), or feature request please use [StackOverflow](http://stackoverflow.com/questions/tagged/semantic-ui) to find a solution.

Visit our [contributing guide](https://github.com/Semantic-Org/Semantic-UI/blob/master/CONTRIBUTING.md) for more on what should be posted to GitHub Issues.

## Install

#### Recommended Install
```bash
npm install semantic-ui  # Use themes, import build/watch tasks into your own gulpfile.
```

Semantic UI includes an interactive installer to help setup your project.

* For more details on setup visit our [getting started guide](http://semantic-ui.com/introduction/getting-started.html).
* To learn more about theming please read our [theming guide](http://www.semantic-ui.com/usage/theming.html)

#### Additional Versions

Environment | Install Script | Repo
--- | --- | --- |
CSS Only | `npm install semantic-ui-css` | [CSS Repo](https://github.com/Semantic-Org/Semantic-UI-CSS)
[LESS](https://github.com/less/less.js/) Only | `npm install semantic-ui-less` | [LESS Repo](https://github.com/Semantic-Org/Semantic-UI-LESS)
[LESS](https://github.com/less/less.js/) plugin | `npm install less-plugin-semantic-ui` | [LESS Plugin Repo](https://github.com/bassjobsen/less-plugin-semantic-ui/)
[EmberJS](http://emberjs.com/) | `ember install:addon semantic-ui-ember` | [Ember Repo](https://github.com/Semantic-Org/Semantic-UI-Ember)
|[Meteor](https://www.meteor.com/) - [LESS](https://github.com/less/less.js/) | `meteor add semantic:ui` | [Meteor Repo](https://github.com/Semantic-Org/Semantic-UI-Meteor) |
|[Meteor](https://www.meteor.com/) - CSS | `meteor add semantic:ui-css` | [CSS Repo](https://github.com/Semantic-Org/Semantic-UI-CSS) |
[Bower](http://bower.io/) | `bower install semantic-ui` |

Check out our [integration wiki](https://github.com/Semantic-Org/Semantic-UI/wiki/Integration) for more options.

#### Browser Support

* Last 2 Versions FF, Chrome, Safari Mac
* IE 11+
* Android 4.4+, Chrome for Android 44+
* iOS Safari 7+
* Microsoft Edge 12+

Although some components will work in IE9, [grids](http://semantic-ui.com/collections/grid.html) and other [flexbox](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Flexible_boxes) components are not supported by IE9 and may not appear correctly.

## Community

#### Getting Help
Please **do not post** usage questions to GitHub Issues. For these types of questions use our [Gitter chatroom] or [StackOverflow](http://stackoverflow.com/questions/tagged/semantic-ui).

#### Submitting Bugs and Enhancements
[GitHub Issues](https://github.com/Semantic-Org/Semantic-UI/issues) is for suggesting enhancements and reporting bugs. Before submiting a bug make sure you do the following:
* Check out our [contributing guide](https://github.com/Semantic-Org/Semantic-UI/blob/master/CONTRIBUTING.md) for info on our release cycle.
* [Fork this boilerplate JSFiddle](https://jsfiddle.net/ca0rovs3/) to create a test case for your bug. If a bug is apparent in the docs, that's ok as a test case, just make it clear exactly how to reproduce the issue. Only bugs that include a test case can be triaged.


#### Pull Requests

When adding pull requests, be sure to merge into the [next](https://github.com/Semantic-Org/Semantic-UI/tree/next) branch. If you need to demonstrate a fix in ``next`` release, you can use [this JSFiddle](https://jsfiddle.net/ca0rovs3/)


#### International

* **Chinese** A Chinese mirror site is available at [http://www.semantic-ui.cn](http://www.semantic-ui.cn).
* **Right-to-Left (RTL)** An RTL version can be created using our build tools by selecting `rtl` from the install script.
* **Translation** To help translate see the [Wiki Guide](https://github.com/Semantic-Org/Semantic-UI/wiki/Translating-Semantic-UI-Docs) for translations.

#### Resources

Resource | Description
--- | --- |
Bugs & Feature Requests |  All bug submission **require** a link to a test case, and a set of steps to reproduce the issue. You can make a test case by forking this [JSFiddle](https://jsfiddle.net/ca0rovs3/), then submit your [bug report on GitHub Issues](https://github.com/Semantic-Org/Semantic-UI/issues)
Live Chat | Join our [Gitter.im Room](https://gitter.im/Semantic-Org/Semantic-UI)
Newsletter Updates | Sign up for updates at [semantic-ui.com](http://www.semantic-ui.com)
Additional Resources  | Submit a question on [StackOverflow](http://stackoverflow.com/questions/tagged/semantic-ui) or ask our [Google Group](https://groups.google.com/forum/#!forum/semantic-ui)

#### Places to Help

Project | How To Help | Next Step
--- | --- | --- |
Localization | Help us translate Semantic UI into your language | [Join our Translation Community](https://github.com/Semantic-Org/Semantic-UI/wiki/Translating-Semantic-UI-Docs)
[SCSS](http://sass-lang.com/) | SASS needs PR to support variables inside `@import` | [Add Pull Request](https://github.com/sass/sass/pulls) for [#739](https://github.com/sass/sass/issues/739#issuecomment-73984809)
[Angular](https://angularjs.org/) | Help develop angular bindings | Reach Out on [GitHub Issues](https://github.com/Semantic-Org/Semantic-UI-Angular/issues/8)
Guides & Tutorials | Help write guides and tutorials | [Join the discussion](https://github.com/Semantic-Org/Semantic-UI/issues/1571)

#### Reaching Out

If you'd like to start a conversation about Semantic feel free to e-mail me at [jack@semantic-ui.com](mailto:jack@semantic-ui.com)

[![Flattr This](https://api.flattr.com/button/flattr-badge-large.png)](https://flattr.com/submit/auto?user_id=jlukic&url=https%3A%2F%2Fgithub.com%2Fjlukic%2FSemantic-UI)

<a href="http://packagequality.com/#?package=semantic-ui"><img src="http://npm.packagequality.com/badge/semantic-ui.png"/></a>

