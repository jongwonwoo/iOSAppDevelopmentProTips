# Pro Tips for iOS App Development

## Memory Leaks

### View Controller를 새로 만들면 Xcode의 메모리 그래프 디버깅 툴로 해제되지 않은 메모리가 있는지 확인한다.
새로 만든 VC를 열었다 닫았는데 메모리 그래프에 VC가 남아있거나, VC에서 사용한 뷰나 모델 등의 인스턴스가 남아있다면 뭔가 잘못된 것이다. 클로저가 있다면 캡쳐된게 있는지, 순환 참조가 있다면 weak나 unowned가 적절하게 쓰였는지 등을 확인한다.
