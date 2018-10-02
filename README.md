# UIAlertController-TextAlignment

var titleString = "Your Message"
if #available(iOS 8.0, *)
{
 
            let alertController = UIAlertController(title: ApplicationName, message: titleString, preferredStyle: .alert)
            
            let OKAction = UIAlertAction(title: "OK", style: .cancel) { (action) in
                alertController.dismiss(animated: true, completion: nil)
            }
            alertController.addAction(OKAction)
            
            let paragraphStyle = NSMutableParagraphStyle()
            paragraphStyle.alignment = NSTextAlignment.left
            
            let messageText = NSMutableAttributedString(
                string: titleString
            )
            
            alertController.setValue(messageText, forKey: "attributedMessage")
            self.present(alertController, animated: true, completion: nil)
        }
        else {
            // Fallback on earlier versions
        }
