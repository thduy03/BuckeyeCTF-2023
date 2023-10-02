## Replace me
![image](https://github.com/thduy03/BuckeyeCTF-2023/assets/126741377/34add0fa-3e5b-4cc3-ac50-9b77751a5f10)
### Solution
We received a file named `dist`. First, we need to find which type is this file using `file`:
![enter image description here](https://i.imgur.com/NbA607S.png)

Next, use `binwalk` to analyze the file:
![enter image description here](https://i.imgur.com/e7vWsnq.png)

There some files were hidden in the original `dist` so lets extract it using `binwalk -e`:
![enter image description here](https://i.imgur.com/TGFj82r.png)

After finding in the extracted folder, we will find an image contains the flag at `/_dist.extracted/5BC000 (1)/res/images/charger/`:
![enter image description here](https://i.imgur.com/cLCwTdz.png)

Flag: `bctf{gr33n_r0b0t_ph0N3}`
