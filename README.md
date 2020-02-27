# CustomCallbackAndroid
Create custom callback method in android

Step 1: Create The callback interface in your 'FromClass'

Step 2: Create an object for your callback Interface inside your 'FromClass'

Step 3: Call the callback method whenever you want to send to execute in your 'FromClass'

Step 4: Define the callback method description in your 'ToClass'.

--------------------------------------------------------------------------------------------------------------------------------

class FromOfCallback {

    // Create an object for interface
   DemoCallbackInterface objDemoCallbackInterface;
      //....
      //.....
      //....
      //....
  void onEvent() {
  
          //call the callback method in any events or whenever you want
          
  callback.callbackCall();
  
  }

    // Create The callback interface in your From class
  interface DemoCallbackInterface {
  
   void demoMethodCallback();
  }
}

//Perform the Callback in your 'ToClass'
// Option 1:

class ToClass implements DemoCallbackInterface {
   void demoMethodCallback() {
      // callback code goes here
   }
}

FromClass.objDemoCallbackInterface = new DemoCallbackInterface();

// Option 2:

FromClass.objDemoCallbackInterface = new DemoCallbackInterface() {

   void demoMethodCallback() {
      // callback code goes here
   }
};
