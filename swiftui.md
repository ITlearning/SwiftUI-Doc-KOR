---
description: Introducing SwiftUI
---

# SwiftUI 소개

> 원문: [https://developer.apple.com/documentation/swiftui/](https://developer.apple.com/documentation/swiftui/)

#### Framework

## SwiftUI

각 플랫폼별(on every platform)로 앱의 사용자 인터페이스와 동작 방식을 선언합니다.

> **지원하는 OS 버전**
>
> iOS 13.0+
>
> iPadOS 13.0+
>
> macOS 10.15+
>
> Mac Catalyst 13.0+
>
> tvOS 13.0+
>
> watchOS 6.0+

#### Overview

SwiftUI는 앱의 **사용자 인터페이스를 선언하기 위한 뷰, 컨트롤 및 레이아웃 구조를 제공**합니다.&#x20;

이 프레임워크는 탭, 제스처 및 기타 유형의 입력을 앱으로 전달하는 이벤트 핸들러를 제공하며, 사용자가 보고 상호작용하는 뷰와 컨트롤에 대한 데이터 흐름을 앱의 모델로부터 관리하는 도구도 제공합니다.

[App](app-structure/undefined/app/) 프로토콜을 사용하여 앱 구조를 정의하고, 앱의 사용자 인터페이스를 구성하는 뷰들을 포함하는 장면들로 채웁니다. View 프로토콜을 따르는 UI를 만들고, SwiftUI 뷰들과 함께 텍스트, 이미지 및 스택과 리스트 등을 이용하여 조합합니다.

내장된 뷰와 자신만의 뷰에 파워풀한 modifier들을 적용하여 렌더링 및 상호 작용을 사용자가 커스텀할 수 있습니다. 컨텍스트와 프레젠테이션에 맞게 조정되는 뷰와 컨트롤로 여러 플랫폼의 앱 간 코드를 공유할 수 있습니다.

<figure><img src=".gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

SwiftUI의 뷰에 UIKit, AppKit, WatchKit 프레임워크의 객체와 통합하여 플랫폼별 기능을 더욱 활용할 수 있습니다. 또한 SwiftUI에서 접근성 지원을 커스텀하여 다른 언어, 국가 또는 문화 지역에 대한 앱 인터페이스를 로컬라이징할 수 있습니다.
