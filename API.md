# API
**NOTE: This API is WIP! Methods might not exist at this point**

# Initializing
```
P2PLink.settings({
  //specify your settings here
})
```
This will initialize an instance of P2PLink and replace all links (can be used only once)

Another way is to provied an object with that information
```
window.P2PLink_settings={
  //specify your settings here
}
```
This works even if you are using the script async

## Networks
### ZeroNet
 - `sources` (Array, default=`['proxy']`, possible=`['local', 'proxy', 'howto']`)
  - Define which sources in which order should be tried
   - Local: The script will try to detect a running instance of ZeroNet and open the link (this might fail even if a local instance is running)
   - Proxy: The script will try to find a proxy to view that link
   - HowTo: A message will be shown how to install and run ZeroNet (This can't be used at the and as the only instruction)
 - `proxies` (Array)
  - Defines which proxies should be used. List can be found in the source code.

# Linking
### An example
`<a href="mkg20001.bit" data-p2p="true" data-type="zeronet" data-show_icon="true">Some website</a>`

This will result in a p2p link (`data-p2p="true"`) that points to the ZeroNet (`data-type="zeronet"`) address mkg20001.bit (`href="mkg20001.bit"`) and a small ZeroNet icon will be shown (`data-show_icon="true"`)

### Properties
 - `data-p2p` (Boolean)
  - Must be true
 - `data-type` (String)
  - Type of the p2p network
 - `data-show_icon`
  - Show an icon of the p2p network (optional)
 - `href`
  - Link to the p2p resource (without additional things like "localhost:port")
  - This will be overwritten by js onclick
