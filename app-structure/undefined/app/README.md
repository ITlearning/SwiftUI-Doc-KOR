---
description: App
---

# App

> 원문: [https://developer.apple.com/documentation/swiftui/app](https://developer.apple.com/documentation/swiftui/app)

#### Protocol

## App

앱의 구조와 동작을 나타내는 타입

> **지원하는 OS 버전**
>
> iOS 14.0+
>
> iPadOS 14.0+
>
> macOS 11.0+
>
> Mac Catalyst 14.0+
>
> tvOS 14.0+
>
> watchOS 7.0+
>
> visionOS 1.0+ <mark style="color:blue;">Beta</mark>

```swift
protocol App
```

***

### Overview

App 프로토콜을 준수하는 구조를 선언하여 앱을 만듭니다. 필수적으로 구현해야 하는 [body](https://app.gitbook.com/o/HZQEGQf5bCI1E71bQnIw/s/KvIlBrraYc6g2lvAGIGM/\~/changes/13/app-structure/undefined/app/body) 프로퍼티에 앱의 컨텐츠를 구현해보세요.

구현의 예시는 다음과 같습니다.

```swift
@main
struct MyApp: App {
    var body: some Scene {
        WindowGroup {
            Text("Hello, world!")
        }
    }
}
```

@main attribute를 구조체 앞에 두어 사용자가 정의한 App 프로토콜을 따르는 구조를 가진 앱에 시작지점을 알려주는 역할을 합니다. App 프로토콜은 시스템이 앱을 실행시킬 때 호출하는 [main()](https://app.gitbook.com/o/HZQEGQf5bCI1E71bQnIw/s/KvIlBrraYc6g2lvAGIGM/\~/changes/13/app-structure/undefined/app/static-func-main) 메서드의 기본 구현을 제공합니다. 앱의 모든 파일 중 정확히 하나의 진입점을 가질 수 있습니다.

App의 body는 [Scene](https://app.gitbook.com/o/HZQEGQf5bCI1E71bQnIw/s/KvIlBrraYc6g2lvAGIGM/\~/changes/13/app-structure/scenes/scene) 프로토콜을 준수하는 인스턴스로 구성됩니다. 각각의 Scene은 뷰 계층 구조의 루트 뷰를 포함하며, 시스템이 관리하는 라이프 사이클을 가집니다. SwiftUI는 문서나 설정을 표시하는 것과 같은 일반적인 시나리오를 처리하기 위한 구체적인 장면 타입을 제공합니다. 사용자 지정 장면을 만들 수도 있습니다.&#x20;

```swift
@main
struct Mail: App {
    var body: some Scene {
        WindowGroup {
            MailViewer()
        }
        Settings {
            SettingsView()
        }
    }
}
```

앱에서 모든 장면에 걸쳐 공유할 상태를 선언할 수 있습니다. 예를 들어, StateObject 속성을 사용하여 데이터 모델을 초기화한 다음, 그 모델을 ObservedObject로 뷰 입력에 제공하거나 앱의 scene에 EnvironmentObject로 environment를 통해 제공할 수 있습니다.

```swift
@main
struct Mail: App {
    @StateObject private var model = MailModel()

    var body: some Scene {
        WindowGroup {
            MailViewer()
                .environmentObject(model) // Passed through the environment.
        }
        Settings {
            SettingsView(model: model) // Passed as an observed object.
        }
    }
}
```

