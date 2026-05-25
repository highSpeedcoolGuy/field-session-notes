# Documentation for connecting to mines global protect vpn on Arch

1. Install [globalprotect-openconnect](https://github.com/yuezk/GlobalProtect-openconnect#arch-linux--manjaro)
    > ``` yay -S globalprotect-openconnect-git ```
2. Launch gui
    > ``` gpclient launch-gui ```
	> Should look something like this: ![[Pasted image 20260524103935.png]]    
3. You may not have to do this but if it's giving errors with regards to OpenSSL or TLS, then enable these two options:
    >  ![[Pasted image 20260524104236.png]]
4. Now you're ready to connect. 
    > Enter `globalprotect.mines.edu` under Portal Address.

5. Now test if you still have connection to your home ip gateway, if not. Check it using:
    > ``` ip route ```
    The default should look like your home gateway and if it's not, remove the vpn gateway from being default:
    > ``` sudo nmcli connection modify "vpn-name-from-ip-route" ipv4.never-default yes ```
    Do the same with ipv6 if you're also using that:
    > ```  sudo nmcli connection modify "vpn-name-from-ip-route" ipv6.never-default yes ```

6. Now test your internet connection again.

Once that's good you can now move on to connecting to a mines server or gateway, here are the steps:

1. If you're doing this from somewhere far from Mines network (which you most likely will be if you're looking at this), you need to use a jumpbox:

    > ``` ssh -J username@jumpbox.mines.edu username@server-name.mines.edu ```
    
    [!NOTE]
    > The two known servers at Mines for use for students and researches are *isengard* and *wendian*.


More links on connecting to mines vpn.
[Mines IT - How to connect to global protect vpn](https://helpcenter.mines.edu/TDClient/1946/Portal/KB/Article/154280/How-to-Connect-to-Global-Protect-VPN-using-an-Unmanaged-or-Personal-Computer)

