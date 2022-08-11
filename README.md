# swift notes to myself

 -DarkMode
 -PlaySound
 -ImageFromUrl
 -PhoneVibration
 -DispatchQueue
 -StatusBar
 -StringFormat
 -RotateImage
 -ImageXYCordinate
 -segmentController


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
        overrideUserInterfaceStyle = .light 
       
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
       rightChatBox.layer.cornerRadius = 20
       rightChatBox.layer.masksToBounds = true
    
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
    
      func scrollToBottom(){
        DispatchQueue.main.async {
            let indexPath = IndexPath(row: myChat.johnChat.count-1, section: 0)
            self.messageTableView.scrollToRow(at: indexPath, at: .bottom, animated: true)
        }
    }
    //-------------SEGMENTCONTROLLER-----------------------
    switch segmentControlOutlet.selectedSegmentIndex {
        case 0:
            uiViewOutlet.backgroundColor = .red
            segmentControlOutlet.backgroundColor = .red
        case 1 :
            uiViewOutlet.backgroundColor = .green
            segmentControlOutlet.backgroundColor = .green
        case 2:
            uiViewOutlet.backgroundColor = .blue
            segmentControlOutlet.backgroundColor = .blue
        default:
            break
        }
    //------------------------------------
    
    
    @objc func keyboardWillShow(notification: NSNotification) {
        view.frame.origin.y = 0
        if let keyboardFrame: NSValue = notification.userInfo?[UIResponder.keyboardFrameEndUserInfoKey] as? NSValue {
            let keyboardRectangle = keyboardFrame.cgRectValue
            let keyboardHeight = keyboardRectangle.height
            view.frame.origin.y -= keyboardHeight
            
        }
    }
    
    @objc func keyboardWillHide(notification: NSNotification) {
        view.frame.origin.y = 0
    }
    
    private func setupKeyboardHiding() {
        NotificationCenter.default.addObserver(self, selector: #selector(keyboardWillShow), name: UIResponder.keyboardWillShowNotification, object: nil)
        NotificationCenter.default.addObserver(self, selector: #selector(keyboardWillHide), name: UIResponder.keyboardWillHideNotification, object: nil)
    }
