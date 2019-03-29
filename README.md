#  iOS Study Project -> Rap Music (打击音乐器)

通过这个项目，学到的东西有：

1. 如何 copy 媒体资源到 project，删除的时候，最好先 remove references ？？？ 直接删除到垃圾桶的话，会出现还在列表，却不在文件夹中的情况，不得不吐槽一下，xcode 这个文件管理真是太难用了

2. 如何使用 do try catch 进行异常的捕捉处理，防止程序在运行时 crash

    ```swift
    func playSound(soundFileName: String) {
    
    let soundURL = Bundle.main.url(forResource: soundFileName, withExtension: "wav")
    
    do {
    try audioPlayer = AVAudioPlayer(contentsOf: soundURL!)
    }catch {
    print(error)
    }
    
    audioPlayer.play()
    }
   ``` 
   
   3. 如何为多个 Button 添加同一个 @IBAction，xcode 在事件绑定这个上面做的的却很智能，拖拖拽拽就完成了页面元素的获取与事件的绑定，熟练操作之后，非常的便捷

