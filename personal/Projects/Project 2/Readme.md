# Payment UPI QR Code Generator

You can generate QR code of your business Payment UPI with custom **Amount**
There are __Three__ variables,One is **Amount value**,  `your_UPI_ID` and another one is `your_name`.

## Example:-

Change this,
* `<your_UPI_ID>` to qape40@testupi
* `<your_name>` to James

This is full link`upi://pay?pa=<your_UPI_ID>&am=${qrValue}&pn=<your_name>`
---> `upi://pay?pa=qape40@testupi&am=${qrValue}&pn=James`
***
> https://chart.googleapis.com/chart?cht=qr&choe=UTF-8

As of now, I am using this Google API to Generate QR image, but according to documentation, it is deprecated.
In future release, I will change this with JS Library by **Nayuki**

## Disclaimer
This project is provided as-is, and we make no guarantees that it will be suitable for your needs. Use at your own risk.
#### Inspired by [CodingNepal](https://www.codingnepalweb.com) and [Nayuki](http://nayuki.io)
