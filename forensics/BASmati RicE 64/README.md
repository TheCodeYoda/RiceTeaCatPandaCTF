This was a pretty well constructed challenge for 150 points.The file supplied to us was a .jpg file with a hint saying that the flag is hidden somewhere in the rice bowl.Seeing the title of the challende "BASE 64" is in CAPS so There is a base64 string hidden in the jpg file. We run steghide -extract -sf <filename> to extract hidden files.Voila! We find a file named "stegopayload..".txt running base64 on the txtfile reveals the flag. we just have to wrap the flag around rtcp{} and replace all z's with "_".

FLAG:"s0m3t1m35zth1ng5zAr3z3nc0D3d"
