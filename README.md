<div align="center">

## Download a web page to a string or a web binary to a byte array


</div>

### Description

Downloads a URI directly into a string or a web binary to a byte array.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Jon Davis](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/jon-davis.md)
**Level**          |Beginner
**User Rating**    |4.5 (18 globes from 4 users)
**Compatibility**  |C\#
**Category**       |[Internet/ Browsers/ HTML](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/internet-browsers-html__10-9.md)
**World**          |[\.Net \(C\#, VB\.net\)](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/net-c-vb-net.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/jon-davis-download-a-web-page-to-a-string-or-a-web-binary-to-a-byte-array__10-295/archive/master.zip)





### Source Code

```
public static string StringFromURL(string URL) {
	System.Net.WebClient WC = new System.Net.WebClient();
	System.IO.StreamReader sr = new System.IO.StreamReader(StreamFromURL(URL));
	return sr.ReadToEnd();
}
public static byte[] BinFromURL(string URL) {
	System.IO.BinaryReader br = new System.IO.BinaryReader(StreamFromURL(URL));
	return br.ReadBytes((int)br.BaseStream.Length);
}
public static System.IO.Stream StreamFromURL(string URL) {
	System.Net.WebClient WC = new System.Net.WebClient();
	return WC.OpenRead(URL);
}
```

