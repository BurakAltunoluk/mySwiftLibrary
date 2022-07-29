# mySwiftLibrary

 -DarkMode
 -PlaySound
 -ImageFromUrl
 -PhoneVibration
 -DispatchQueue
 -StatusBar
 -StringFormat
 -RotateImage
 -ImageXYCordinate


```swift

  //----------- Dark Mode : -----------------
  
  let userInterfaceStyle = traitCollection.UserInterfaceStyle
  
  if userInterFaceStyle == .dark {
  //code
  }

  //---
  
  override func traitCollectionDidChange( _ previousTraitCollection: UITraitCollection?) {
  
  
  
  }
  //---
  
      override func viewDidLoad() {
        super.viewDidLoad()
        overrideUserInterfaceStyle= .light 
       
    }
  //---
  
  info.playlist 
  userInterfaceStyle = .dark
                       .light

  //--------------playSound--------------------

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
    //------------- image from url  ---------------------
    
    let urlString = "https://..............jpeg"
    let imageData = try! Data(contentsOf:URL(string: urlStrings!)!)
    imageView.image = UIimage(data: datam)
    
    //----------------------------------
    
    if df == nil ? 0 : 1
    
    //------------------------------------
    
    
    let duration = String(format: "%.01f",3,32210)   //output 3.3
    
    //------------------------------------
    
    import AudioToolbox
    
    AudioServicesPlayAlertSound(1521)
    
    
    
    //------------------------------------
    
    image.frame.origin.x = 20
    image.frame.origin.x = 40
    
    
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
