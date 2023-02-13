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
 -NotificationCenter
 -Blur affect
 -TextToSpeech
 -Text Replacing
 -CornerRadiusImage
 -encode URL utf8  

https://app.quicktype.io/


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
    
    let contentHeight = 40
    let hasHeader = true
    let rowHeight = contentHeight + (hasHeader ? 50 : 20)
    // rowHeight is equal to 90
    
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
    
    
    //-------NotificationService-------------
    
    // sendNotification 
     NotificationCenter.default.post(name: Notification.Name("done"), object: nil)
     
     //ReceiveNotification
     NotificationCenter.default.addObserver(self, selector:#selector(doneResponse) , name: Notification.Name("done"), object: nil)
     
     @objc func doneResponse() {
       
     }
    //-----Blur Affect-----------------------
    
       
    func blurEffect() {
        
        let blurEffect = UIBlurEffect(style: UIBlurEffect.Style.light)
        let blurEffectView = UIVisualEffectView(effect: blurEffect)
        blurEffectView.frame = view.bounds
        blurEffectView.autoresizingMask = [.flexibleWidth, .flexibleHeight]
        view.addSubview(blurEffectView)
    }
    
    func removeBlurView() {
        for subview in view.subviews {
            if subview.isKind(of: UIVisualEffectView.self) {
                subview.removeFromSuperview()
            }
        }
    }
    //-------------Extra Blur Affect---------
   // self.view.backgroundColor = UIColor().transparentBlur()
 //   You will need to create the blur effect using the UIBlurEffect Class in the viewDidLoad method. After that you’ll need to apply the effect to the //UIVisualEffectView.

//The UIVisualEffectView needs to have the container dimensions defined, and it will be the first view of the stack of the view controller.

let blurEffect = UIBlurEffect(style: .ExtraLight) 
let blurEffectView = UIVisualEffectView(effect: blurEffect) 
blurEffectView.frame = self.view.frame 
self.view.insertSubview(blurEffectView, atIndex: 0

    //-------------------------------------
    
    //--------textToSpeech-----------------
    
      private func textToSpeech(choosedRow: String) {
        let string = choosedRow
        let utterance = AVSpeechUtterance(string: string)
        utterance.voice = AVSpeechSynthesisVoice(language: "en-GB")
        let synth = AVSpeechSynthesizer()
        synth.speak(utterance)
    }
    
    //--------------Text Replacing----------------
    
    var testString = "Hello world"
    testString.replacingOccurrences(of: " ", with: "%20")
    
    //--------------------------------------
    //-----------Corner Radius Image --------
    
      plusButtonImage.layer.cornerRadius = 30
      plusButtonImage.clipsToBounds = true
    
    //--------------------------------------
    
    //----------- encode URL utf8   -------------
    
        let output = self.wordInputTextFiled.text!.addingPercentEncoding(withAllowedCharacters: .urlHostAllowed)! as String
    
    
    //--------------------------------------
