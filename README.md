# HideOnImage

`HideOnImage`는 얼굴인식 자동모자이크 라이브러리입니다. 자동으로 이미지의 얼굴을 인식하고 모자이크 처리해줍니다.

## 설치
Swift Package Manager(SPM)에 다음 Package URL로 사용할 수 있습니다.
```
https://github.com/January1st-98/HideOnImage.git
```

## 사용법
- Mosaic 인스턴스를 생성한다.
- Mosaic 인스턴스의 `delegate`를 현재 처리할 뷰 컨트롤러로 지정합니다.
- `UIImage`이미지 데이터를 `convert(with:)`메서드의 파라미터로 넘겨 모자이크 이미지로 변환을 시작합니다.
- `MosaicDelegate` 프로토콜의 Delegate 메서드를 구현한다.
- `mosaicImageProcessDidFinish` delegate 메서드의 파라미터로 주어지는 결과 이미지를 사용한다.
```swift
let mosaic = Mosaic()
mosaic.delegate = self

let image = UIImage(named: "my-image")
mosaic.convert(with: image)

...

extension class_name: MosaicDelegate {

    func mosaicImageProcessDidFinish(with result: UIImage) {
        self.imageView.image = result
    }
}
```
---

HideOnImage is a face detection automatic mosaic library. It automatically recognizes and mosaic the face of the image.

## Installation
Available in Swift Package Manager (SPM) as the following package URL
```
https://github.com/January1st-98/HideOnImage.git
```
