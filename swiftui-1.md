---
description: SwiftUI updates
---

# SwiftUI 업데이트 로그

> 원문: [https://developer.apple.com/documentation/updates/swiftui](https://developer.apple.com/documentation/updates/swiftui)

#### Article

## SwiftUI updates

SwiftUI의 중요한 업데이트에 대해 알아봅니다.

### Overview

SwiftUI 중요한 업데이트 사항에 대해 훑어봅니다.

### 2023년 6월, visionOS

**Scenes**

* 앱 화면에 volumetric 윈도우 스타일을 적용하여 3D 모델을 표시할 수 있는 볼륨을 생성합니다.
* 전체 공감을 활용하여 ImmersiveSpace Scene을 열어보세요. mixed 몰입 스타일을 사용하여 객체들을 사용자 주변에 배치하거나, 완전한 스타일로 시각적 경험을 제어할 수 있습니다.
* RealityKit의 Model3D 또는 RealityView 구조체를 사용하여 볼륨이나 전체 공간에서 3D 모델을 표시하세요. 이 Framework의 엔티티를 로드하여 사용할 수 있습니다.

**Toolbars and ornaments**

* bottomOrnament 툴바 아이템 배치를 사용하여 툴바 항목을 장식으로 표시하세요.
* ornament(visibility:attachmentAnchor:contentAlignment:ornament:) 뷰 수정자를 사용하여 창에 직접 장식을 추가하세요.

**Drawing and graphics**

* GeometryReader3D를 사용하여 세 가지 차원에서 뷰의 지오메트리를 감지하세요.
* 3D 효과를 visualEffect3D(\_:) 뷰 모디파이어를 사용하여 추가하세요.
* 각각 rotation3DEffect(\_:anchor:)와 scaleEffect(x:y:z:anchor:)와 같은 뷰 모디파이어를 사용하여 세 가지 차원에서 회전하거나 크기를 조정하세요.
* PhysicalMetricsConverter를 사용하여 화면 표시 점과 물리적 거리 간의 변환을 수행하세요.

**View Configuration**

* glassBackgroundEffect(displayMode:) 뷰 모디파이어를 사용하여 뷰에 유리같은 백그라운드 효과를 추가하세요.
* 목적에 맞는 경우에 따라서 preferredSurroundingsEffect(\_:) 모디파이어를 적용하여 통과 시키면서 어둡게 표시하세요.

**View layout**

* offset(z:) 및 padding3D(\_:), frame(depth:alignment:)과 같은 뷰 모디파이어를 사용하여 3D 레이아웃에 대한 조절을 해보세요.

**Gestures**

* RotateGesture3D 제스처를 추가하여 사용자들이 객체를 세 가지 차원에서 회전할 수 있도록 가능하게 만드세요.

### 2023년 6월

**Scenes**

* environment에 저장된 dismissWindow 액션을 사용하여 identifier에 따라서 Window를 닫을 수 있어요.
* SettingsLink 버튼을 표시하여 사용자가 설정 창을 열 수 있도록 가능하게 만드세요.

**Navigation**

* navigationDestination(item:destination:) 뷰 모디파이어의 새로운 오버로드를 사용하여 네비게이션 스플릿 뷰 또는 스택의 뷰들을 제어하세요.

**Modal presentations**

* 새로운 오버로드인 fileExporter(isPresented:document:contentTypes:defaultFilename:onCompletion:onCancellation:)를 사용하여 파일 내보내기, 가져오기, 이동 모디파이어의 새로운 기능에 접근하세요. 이를 통해 다음과 같은 파일 관리 기능을 활용할 수 있습니다.
  * 기본 디렉터리에서 파일 가져오기 또는 내보내기 대화 상자를 구성하고, 특정 파일 형식만 허용하며, 숨겨진 파일을 표시하도록 설정하세요.
  * 유저가 선택한 파일 인터페이스 구성을 다음 프레젠테이션에 유지하세요.
  * Transferable 프로토콜을 준수하는 유형들을 내보냅니다.
* 다이얼로그 심각도를 지정하려면 dialogSeverity(\_:) 뷰 모디파이어를 사용하세요.
* 다이얼로그에 사용자 정의 아이콘을 제공하려면 dialogIcon(\_:) 모디파이어를 사용하세요.
* dialogSuppression(\_:isSuppressed:)와 같은 다이얼로그 억제 모디파이어 중 하나를 사용하여 다이얼로그를 억제할 수 있도록 허용하세요.

**Toolbars**

* toolbarTitleDisplayMode(\_:) 모디파이어를 사용하여 툴바 제목의 표시 크기를 구성하세요.

**Search**

* searchable(text:isPresented:placement:prompt:)와 같은 일부 검색 가능한 뷰 모디파이어에서 사용 가능한 새로운 isPresented 매개변수에 바인딩을 사용하여 검색을 프로그래밍 방식으로 표시하세요.
* searchable(text:editableTokens:isPresented:placement:prompt:token:)와 같은 해당하는 검색 가능한 뷰 모디파이어에서 token 클로저의 입력에 바인딩을 제공하여 변경 가능한 검색 토큰을 생성하세요.

**Data and storage**

* SwiftUI 환경 키와 UIKit 특성 간에 더 쉽게 연결하기 위해 UITraitBridgedEnvironmentKey 프로토콜을 사용하세요.
* 새로운 doc://com.apple.documentation/documentation/Observation/Observable-swift.macro 매크로를 사용하여 앱 전체에 데이터를 공유할 때 더 나은 성능을 얻으세요.
* onChange(of:initial:\_:) 뷰 모디파이어의 완료 클로저를 처리할 때 값이 변경되는 값의 이전 값과 새로운 값을 모두 접근하세요.

**Views**

* 리소스(예: 검색 결과 또는 네트워크 연결)가 사용 불가능할 때 ContentUnavailableView 뷰 타입을 사용하여 표준 인터페이스를 표시하세요.
* inspector(isPresented:content:) 모디파이어를 적용하여 플랫폼에 적합한 외관을 가진 표준 검사자(Inspector) 인터페이스를 표시하세요.

**Animation**

* 애니메이션이 완료될 때 액션을 수행하려면 withAnimation(_:completionCriteria:_:completion) 모디파이어에 완료 클로저를 지정하세요.
* CustomAnimation 프로토콜을 준수하는 타입을 생성하여 사용자 정의 애니메이션 동작을 정의하세요.
* Predefined phase를 통해 진행되는 애니메이션을 PhaseAnimator 구조체를 사용하여 수행하거나, Keyframes 프로토콜을 사용하여 시간 기반 키프레임의 집합에 따라 애니메이션을 수행하세요.
* Custom TransactionKey 인스턴스를 사용하여 상태 변화에 관한 정보를 지정하세요. 이를 통해 특정 애니메이션을 요청할 수 있습니다.
* UnitCurve를 사용하여 사용자 정의 애니메이션 곡선을 디자인하세요.
* 새로운 spring(duration:bounce:blendDuration:) 애니메이션을 사용하여 모든 Apple 프레임워크에서 표준화된 간소화된 스프링 매개변수를 적용하세요. 또한 Spring 구조체를 사용하여 스프링의 동작을 편리하게 표현할 수도 있습니다.

**Text input and output**

* Text 뷰에서 표시되는 언어를 typesettingLanguage(\_:isEnabled:) 모디파이어를 사용하여 지정하여 SwiftUI가 텍스트의 잘림과 충돌을 피하고 적절한 줄 바꿈과 분리 기호 처리를 수행할 수 있도록 하세요.
* 텍스트를 의미적으로 확대 또는 축소하려면 textScale(\_:isEnabled:) 수정자를 사용하여 보조 텍스트 크기를 라벨링하세요. 예를 들어, 보조 텍스트 크기로 지정할 수 있습니다.

**Shapes**

* 하나의 Shape에 여러 개의 fill(_:style:) 또는 stroke(_:style:antialiased:) 모디파이어를 적용하세요.
* intersection(_:eoFill:) 및 union(_:eoFill:)과 같은 Boolean 연산을 모양과 패스에 적용하세요.
* rect와 같은 미리 정의된 모양 스타일을 사용하여 코드를 간단하게 만드세요.
* rect(topLeadingRadius:bottomLeadingRadius:bottomTrailingRadius:topTrailingRadius:style:)을 사용하여 각기 다른 모서리가 둥근 사각형을 만드세요.
* 사용자 정의 모양 스타일에 대해 resolve(in:) 메서드를 정의하여 동적인 색상과 렌더링 스타일을 생성하세요.

**Drawing and graphics**

* Shader 구조체를 사용하여 SwiftUI 앱 내에서 Metal 셰이더로 그래픽을 완전히 사용자 정의하고 고성능으로 그릴 수 있습니다.
* allowedDynamicRange(\_:) 모디파이어를 적용하여 이미지의 특정 동적 범위를 구성하세요.
* visualEffect(\_:) 모디파이어를 사용하여 뷰의 기하적 측면에 따라 적용되는 효과를 조합하세요. 예를 들어, 뷰의 디스플레이 내 위치에 따라 다양한 블러 효과를 적용할 수 있습니다.

**Layout**

* CoordinateSpaceProtocol을 사용하여 새로운 GeometryProxy 메서드인 bounds(of:)와 frame(in:)과 함께 사용하여 컨테이너의 차원을 얻기 위해 사용자 정의 좌표 공간을 정의하세요.
* containerRelativeFrame(\_:alignment:)을 사용하여 컨테이너 뷰의 특성을 기반으로 콘텐츠를 배치하는 뷰에 대한 프레임을 생성하세요.
* containerBackground(\_:for:) 뷰 모디파이어를 사용하여 컨테이너 뷰의 배경을 설정하세요.

**Lists and tables**

* List나 Table에서 항목의 선택 가능성을 비활성화하려면 selectionDisabled(\_:) 모디파이어를 적용하세요.
* 리스트나 테이블에서 섹션을 축소 또는 확장하려면 섹션의 초기화 함수에서 isExpanded 바인딩을 사용하세요.
* row나 section 간격을 각각 listRowSpacing(_:)와 listSectionSpacing(_:) 모디파이어로 구성하세요.
* 뱃지의 중요도를 badgeProminence(\_:) 뷰 모디파이어로 설정하세요.
* alternatingRowBackgrounds(\_:) 모디파이어를 사용하여 번갈아가며 로우의 배경을 구성하세요.
* TableColumnCustomization 구조체를 사용하여 테이블의 열 가시성과 재정렬을 사용자 정의하세요.
* DisclosureTableRow 구조체를 사용하여 테이블에 계층적인 로우를 추가하거나, OutlineGroup 구조체를 사용하여 재귀적으로 계층적인 로우를 추가하세요.
* tableColumnHeaders(\_:) 모디파이어를 사용하여 테이블 열 헤더를 숨기세요.

**Scrolling**

* 스크롤 뷰의 위치를 읽으려면 doc://com.apple.documentation/documentation/SwiftUI/View/scrollPosition(id:)와 같은 스크롤 위치 모디파이어 중 하나를 사용하세요.
* scrollIndicatorsFlash(onAppear:)와 같은 뷰 모디파이어를 사용하여 스크롤 인디케이터를 프로그래밍 방식으로 깜박이게 할 수 있습니다.
* scrollClipDisabled(\_) 모디파이어를 사용하여 기본 클리핑을 비활성화한 후 커스텀 방식으로 스크롤 뷰를 클리핑하세요.
* scrollTargetBehavior(\_) 뷰 모디파이어를 사용하여 페이지 또는 뷰 경계에 맞추어 정렬된 페이지식 스크롤 뷰를 생성하세요.
* ScrollTargetBehavior 프로토콜을 사용하여 사용자 정의 스크롤 동작을 생성하세요.
* safeAreaPadding(_)과 contentMargins(_:for:) 뷰 모디파이어를 사용하여 스크롤 가능한 뷰의 여백을 제어하세요.
* scrollTransition(\_:axis:transition:) 모디파이어 중 하나를 사용하여 뷰가 화면에 스크롤되거나 나갈 때 효과를 추가하세요.
* watchOS에서 수직 페이징을 지원하는 TabView를 생성하기 위해 verticalPage 탭 뷰 스타일을 적용하세요.

**Gestures**

* 일부 제스처와 트랜잭션에 관련된 값들에 새로운 velocity 속성을 사용하여 제스처와 애니메이션 사이의 더 부드러운 전환을 만드세요. 또한 Transaction의 tracksVelocity 속성을 사용하세요.
* 더 많은 정보에 접근하려면 이제 더 이상 사용되지 않는 MagnificationGesture와 RotationGesture를 대체하는 새로운 MagnifyGesture와 RotateGesture로 마이그레이션하세요. 이를 통해 속도와 위치를 모두 포함한 더 많은 정보에 접근할 수 있습니다.

**Input events**

* 포커스를 받고 있는 뷰가 키보드 입력에 직접 반응하도록 하려면 onKeyPress(\_:action:) 뷰 모디파이어 중 하나를 적용하세요.
* Picker를 팔레트 스타일로 스타일링하여 메뉴에서 간단한 항목들을 선택할 수 있도록 하세요.
* sensoryFeedback(\_:trigger:)와 같은 감각적 피드백 모디파이어를 사용하여 이벤트에 대한 햅틱 또는 오디오 피드백을 제공하세요.
* 새로운 init(_:intent:)와 init(_:isOn:intent:)와 같은 초기화자를 사용하여 위젯, 라이브 액티비티 및 기타 장소에서 AppIntent를 수행하는 버튼과 토글을 생성하세요.

**Focus**

* 새로운 focusable(\_:interactions:) 뷰 모디파이어를 사용하여 버튼과 같이 주요 액션이 있는 뷰와 텍스트 필드와 같이 입력을 받는 뷰와 같이 포커스가 서로 다른 목적으로 사용되는 뷰를 구분하세요.
* focusEffectDisabled(\_) 모디파이어를 사용하여 뷰가 포커스를 받을 때의 효과를 관리하세요.

**Previews in Xcode**

* 새로운 doc://com.apple.documentation/documentation/SwiftUI/preview(\_:traits:body:) 매크로를 사용하여 Xcode 프리뷰를 생성하는 데 필요한 불필요한 보일러플레이트를 줄일 수 있습니다.

> **각 도큐먼트로 이동하는 링크는 추후 문서에 작성 후 달겠습니다!**
