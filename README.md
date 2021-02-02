--------- Run Website -----

>1. install node 
2. download the source code from github
3. npm init, npm install, npm install ejs, npm install express
4. node index.js
5. browser : 127.0.0.1:3000


-- Xcode Feature --

+ Function userContentController --> listener the post message from website side
+       //Setup communication with Javascript
        let contentController = self.webView.configuration.userContentController
        contentController.add(self, name: "toggleMessageHandler")
        //
+ webView.evaluateJavaScript("someFunctionHere()", completionHandler: nil) -> To trigger the javascript function in website

-- Website Feature --
+       window.webkit.messageHandlers.toggleMessageHandler.postMessage({
                "type": "finishSendToken",
                "msg": "Send token to website successfully",
            });
       -> Define the postmessage to send back to Application (the payload is JSON)    
        
