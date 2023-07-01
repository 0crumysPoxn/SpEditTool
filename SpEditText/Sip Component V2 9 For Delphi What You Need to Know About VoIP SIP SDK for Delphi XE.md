# How to Use Sip Component V2 9 For Delphi
 
Sip Component V2 9 For Delphi is a library of code that allows you to make and answer phone calls in your Delphi applications using the SIP protocol. It consists of three main parts: a SIP stack, an RTP stack, and SDP parsing and utilities. It supports most of the SIP features and RFCs, such as authentication, registration, call transfer, conference calls, text messages, and more.
 
In this article, we will show you how to use Sip Component V2 9 For Delphi to create a simple softphone application that can make and receive calls from other SIP clients. We will assume that you have a SIP account from a provider like VOIP BUSTER, NET-VOICE, OVH Telecom, SIPNET etc. or you have installed a PBX like Asterisk on your computer.
 
**Download ○○○ [https://t.co/zIgx7yr9M4](https://t.co/zIgx7yr9M4)**


 
## Step 1: Install Sip Component V2 9 For Delphi
 
You can download Sip Component V2 9 For Delphi from [https://www.sipcomponents.com/](https://www.sipcomponents.com/). The source code of the component is compatible with all Delphi versions starting from Delphi 5 to latest Delphi Tokyo. You can either install it in your Delphi environment and place it on your form or create it dynamically at runtime.
 
## Step 2: Create an instance of TSipClient
 
TSipClient is the main class of the component that handles all the SIP operations. You need to create an instance of TSipClient and assign the properties from your SIP account and specify event handler procedures. For example:
 `
procedure TForm1.FormCreate(Sender: TObject);
begin
  FSipClient := TSipClient.Create(nil);
  FSipClient.Host := 'sipprovider.com';
  FSipClient.User := 'myusername';
  FSipClient.Password := 'mypassword';
  // Assigning event handler procedures
  FSipCLient.OnRegistration := SipClientRegistration;
  FSipClient.OnCall := SipClientCall;
  FSipClient.OnAnswer := SipClientAnswer;
  FSipCLient.OnBye := SipClientBye;
  FSipCLient.OnPlayed := SipClientPlayed;
  FSipCLient.OnDtmf := SipClientDtmf;
  // Activate the engine
  FSipClient.Active := True;
  // Start registration on SIP serever
  FSipClient.Register;
end;
` 
The event handlers are used to handle different situations that may occur during the SIP communication, such as registration status, incoming calls, outgoing calls, call termination, media playback, user input, etc. You can implement your own logic in these event handlers according to your needs.
 
## Step 3: Make and answer phone calls
 
To make a phone call, you need to use the Call method of TSipClient and pass the destination number as a parameter. For example:
 
Delphi SIP components[^1^],  TSipClient Delphi component[^1^],  Delphi SIP softphone[^1^],  Delphi SIP provider[^1^],  Delphi SIP Asterisk[^1^],  Delphi SIP Components tutorial[^2^],  Delphi SIP Components example[^2^],  Delphi SIP Components VCL[^2^],  Delphi SIP Components multithreaded[^2^],  Delphi SIP Components events[^2^],  Delphi SIP Components registration[^2^],  Delphi SIP Components invite[^2^],  Delphi SIP Components play wav[^2^],  Delphi SIP Components record call[^2^],  Delphi SIP Components end call[^2^],  Delphi SIP Components source code[^2^],  How to use Sip Component V2 9 For Delphi[^3^],  Sip Component V2 9 For Delphi library[^3^],  Sip Component V2 9 For Delphi download[^3^],  Sip Component V2 9 For Delphi features[^3^],  Sip Component V2 9 For Delphi documentation[^3^],  Sip Component V2 9 For Delphi license[^3^],  Sip Component V2 9 For Delphi review[^3^],  Sip Component V2 9 For Delphi support[^3^],  Sip Component V2 9 For Delphi compatibility[^3^],  Sip Component V2 9 For Delphi VOIP BUSTER[^1^] [^3^],  Sip Component V2 9 For Delphi NET VOICE[^1^] [^3^],  Sip Component V2 9 For Delphi OVH Telecom[^1^] [^3^],  Sip Component V2 9 For Delphi SIPNET[^1^] [^3^],  Sip Component V2 9 For Delphi PBX[^1^] [^3^],  Sip Component V2 9 For Delphi DTMF[^1^] [^3^],  Sip Component V2 9 For Delphi TTS[^1^] [^3^],  Sip Component V2 9 For Delphi conference calls[^1^] [^3^],  Sip Component V2 9 For Delphi Tokyo[^1^] [^3^],  Sip Component V2 9 For Delphi Active property[^1^] [^3^],  Sip Component V2 9 For Delphi Call method[^1^] [^3^],  Sip Component V2 9 For Delphi Answer method[^1^] [^3^],  Sip Component V2 9 For Delphi EndCall method[^1
 `
procedure TForm1.CallButtonClick(Sender: TObject);
begin
  FCall := FSipClient.Call('18025551111');
end;
` 
This will initiate a SIP INVITE request to the destination number and return an ICall interface that represents the call object. You can use this interface to access various properties and methods of the call, such as State, Duration, EndCall, Hold, Transfer, etc.
 
To answer an incoming call, you need to use the Answer method of the ICall interface that is passed as a parameter in the OnCall event handler of TSipClient. For example:
 `
procedure TForm1.SipClientCall(Sender: TObject; const ACall: ICall);
begin
  FCall := ACall;
  FCall.Answer;
end;
` 
This will send a SIP OK response to the caller and establish a media session between the two parties.
 
To end a call, you need to use the EndCall method of the ICall interface. For example:
 `
procedure TForm1.HangupButtonClick(Sender: TObject);
begin
  FCall.EndCall;
  FCall := nil;
end;
` 
This will send a SIP BYE request to the other party and terminate the
 8cf37b1e13
 
