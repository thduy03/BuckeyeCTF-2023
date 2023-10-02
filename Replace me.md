## Replace me
![enter image description here](https://i.imgur.com/T0QVOZs.png)
### Solution
We received a file named `dist`. First, we need to find which type is this file using `file`:
![enter image description here](https://i.imgur.com/NbA607S.png)

Next, use `binwalk` to analyze the file:
![enter image description here](https://i.imgur.com/e7vWsnq.png)
We found some files were hidden in the original `dist` so lets extract it using `binwalk -e`:
![enter image description here](https://i.imgur.com/TGFj82r.png)

After finding in the extracted folder, we will find an image contains the flag at `/_dist.extracted/5BC000 (1)/res/images/charger/`:
![enter image description here](https://i.imgur.com/cLCwTdz.png)
Flag: `bctf{gr33n_r0b0t_ph0N3}`
