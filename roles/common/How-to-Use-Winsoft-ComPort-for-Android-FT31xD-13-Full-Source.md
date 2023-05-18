## How to Use Winsoft ComPort for Android FT31xD 1.3 Full Source

  
# How to Use Winsoft ComPort for Android FT31xD 1.3 Full Source
 
Winsoft ComPort for Android FT31xD 1.3 Full Source is a communication library for Delphi and C++ Builder that allows you to connect to FTDI FT311D and FT312D devices on Android. It supports the complete functionality of these devices, such as UART, GPIO, PWM, I2C Master, SPI Slave, and USB to Serial.
 
## Winsoft ComPort for Android FT31xD 1.3 Full Source


[**Download File**](https://www.google.com/url?q=https%3A%2F%2Ftlniurl.com%2F2tKEQa&sa=D&sntz=1&usg=AOvVaw1dv_3XlYEVH4NeEkwgh0uc)

 
In this article, we will show you how to use Winsoft ComPort for Android FT31xD 1.3 Full Source in your Delphi or C++ Builder projects. You will need the following:
 
- An FTDI FT311D or FT312D device with a USB cable
- An Android device with USB OTG support
- A registered version of Winsoft ComPort for Android FT31xD 1.3 Full Source
- Delphi or C++ Builder 10 - 11

First, you need to install the FTDI D2XX driver on your Android device. You can download it from [here](https://www.ftdichip.com/Drivers/D2XX.htm). Follow the instructions on how to install it on your device.
 
Next, you need to add the Winsoft ComPort for Android FT31xD library to your project. You can do this by using the Project Manager or by adding the following line to your source code:

    // Delphi
    uses AComPortFT31xD;
    
    // C++ Builder
    #include <AComPortFT31xD.hpp>

Then, you need to create an instance of the TAComPortFT31xD component and set its properties according to your device configuration. For example:

    // Delphi
    var
      ComPort: TAComPortFT31xD;
    begin
      ComPort := TAComPortFT31xD.Create(Self);
      ComPort.DeviceName := 'UART'; // or 'GPIO', 'PWM', 'I2CM', 'SPIS', 'USBS'
      ComPort.BaudRate := br9600; // or any other supported baud rate
      ComPort.DataBits := db8bits; // or db7bits
      ComPort.Parity := prNone; // or prOdd, prEven, prMark, prSpace
      ComPort.StopBits := sbOne; // or sbOneAndHalf, sbTwo
      ComPort.FlowControl := fcNone; // or fcHardware
    end;
    
    // C++ Builder
    TAComPortFT31xD *ComPort;
    __fastcall TForm1::TForm1(TComponent* Owner): TForm(Owner)
    
      ComPort = new TAComPortFT31xD(this);
      ComPort->DeviceName = "UART"; // or "GPIO", "PWM", "I2CM", "SPIS", "USBS"
      ComPort->BaudRate = br9600; // or any other supported baud rate
      ComPort->DataBits = db8bits; // or db7bits
      ComPort->Parity = prNone; // or prOdd, prEven, prMark, prSpace
      ComPort->StopBits = sbOne; // or sbOneAndHalf, sbTwo
      ComPort->FlowControl = fcNone; // or fcHardware

Finally, you need to open the port and start communicating with your device. You can use the methods and events of the TAComPortFT31xD component to send and receive data. For example:

    // Delphi
    procedure TForm1.ButtonOpenClick(Sender: TObject);
    begin
      if not ComPort.Active then
        ComPort.Open;
    end;
    
    procedure TForm1.ButtonCloseClick(Sender: TObject);
    begin
      if ComPort.Active then
        ComPort.Close;
    end;
    
    procedure TForm1.ButtonSendClick(Sender: TObject);
    var
      Data: TBytes;
    begin
      if ComPort.Active then
      begin
        Data := TEncoding.UTF8.GetBytes(EditSend.Text + #13#10); // append CR LF
        ComPort.Write(Data);
        MemoLog.Lines 0f148eb4a0
