# mySwiftLibrary


```swift

  //----------------------------------

  import UIKit
  import AVFoundation

   class ViewController: UIViewController {
    
   var player: AVAudioPlayer!
    
   func playSound() {
        let url = Bundle.main.url(forResource: "sound1", withExtension: "mp3")
        player = try! AVAudioPlayer(contentsOf: url!)
        player.play()
                
       }
    }
    

    //-------------------------------------

    imageView.transform = imageView.transform.rotated(by: 0.2)
    
    //-------------------------------------

       override var prefersStatusBarHidden: Bool {
        return true
    }

    //-------------------------------------
      
        DispatchQueue.main.asyncAfter(deadline: .now() + 0.2) {
                   //code
           }
        
    //-------------------------------------
