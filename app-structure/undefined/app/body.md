---
description: body
---

# body

#### Instance Property

## Body

앱의 컨텐츠 및 동작

> **지원하는 OS 버전**
>
> iOS 14.0+ | iPadOS 14.0+ | macOS 11.0+ | Mac Catalyst 14.0+ | tvOS 14.0+ | watchOS 7.0+ | visionOS 1.0+

```swift
@SceneBuilder @MainActor @preconcurrency
var body: Self.Body { get }
```

***

### Discussion

**Body**는 앱의 화면을 구성하는 핵심적인 부분을 정의하는 속성입니다. 앱에서 `Body`속성을 사용하여 앱의 **Scene**(장면)을 정의하며, 이 장면들은 [`Scene`](../../scenes/)프로토콜을 준수하는 인스턴스입니다. 예를 들어, 단일 화면과 단일 뷰로 구성된 간단한 앱을 다음과 같이 만들 수 있습니다:&#x20;

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

Swift는 `body` 속성에 제공된 장면(Scene)을 기반으로 앱의 Body 관련 타입을 추론합니다.

> 원문 : [https://developer.apple.com/documentation/swiftui/app/body-swift.property](https://developer.apple.com/documentation/swiftui/app/body-swift.property)
