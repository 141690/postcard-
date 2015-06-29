# postcard-
first rev of project
//
//  ViewController.swift
//  Postcard
//
//  Created by Home on 6/28/15.
//  Copyright (c) 2015 Anna Apps. All rights reserved.
//

import UIKit

class ViewController: UIViewController {
    
    
    @IBOutlet weak var MessageLabel: UILabel!
    @IBOutlet weak var enterNameTextField: UITextField!
    @IBOutlet weak var enterMessageTextField: UITextField!
    @IBOutlet weak var mailButton: UIButton!
    
    @IBOutlet weak var enterNameButton: UILabel!

    override func viewDidLoad() {
        super.viewDidLoad()
        // Do any additional setup after loading the view, typically from a nib.
    }

    override func didReceiveMemoryWarning() {
        super.didReceiveMemoryWarning()
        // Dispose of any resources that can be recreated.
    }

    @IBAction func sendMailButtonPressed(sender: UIButton) {
        MessageLabel.hidden = false
        MessageLabel.text = enterMessageTextField.text
        MessageLabel.textColor = UIColor.blackColor()
        
        enterNameButton.hidden = false
        enterNameButton.text = enterNameTextField.text
        enterNameButton.textColor = UIColor.blackColor()
        
        enterMessageTextField.text = ""
        enterNameTextField.text = ""
        enterMessageTextField.resignFirstResponder()
        
        
        mailButton.setTitle("Mail Sent", forState: UIControlState.Normal)
    }

}
