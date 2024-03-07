<p align="center">
    <img src="./fly-io-logo.svg" alt="fly-io-logo" style="display: block; margin: 0 auto;">
</p>


# Fly.io installation on Mac M1 to get started


the specifications of the device I'm using

    ❯ system_profiler SPSoftwareDataType SPHardwareDataType

        Software:
            System Software Overview:
                System Version: macOS 13.3.1 (22E261)
                Kernel Version: Darwin 22.4.0
                Boot Volume: Macintosh HD
                Boot Mode: Normal    
                . . .

        Hardware:
            Hardware Overview:
                Model Name: MacBook Pro
                Model Identifier: MacBookPro17,1
                Model Number: MYD82ID/A
                Chip: Apple M1
                Total Number of Cores: 8 (4 performance and 4 efficiency)
                Memory: 8 GB
                . . .

---

## Install flyctl

Reference https://fly.io/docs/hands-on/install-flyctl/

run the install script :

      ❯ curl -L https://fly.io/install.sh | sh

            % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                        Dload  Upload   Total   Spent    Left  Speed
        100  1475    0  1475    0     0   4232      0 --:--:-- --:--:-- --:--:--  4287
        ######################################################################## 100.0%


      ❯ ls -lah | grep .fly

        drwxr-xr-x   4 <user>  staff   128B Feb 12 20:05 .fly


      ❯ sudo mv .fly /usr/local/bin/fly

          Password:


      ❯ ls -lah /usr/local/bin | grep fly

        drwxr-xr-x   4 <user>  staff   128B Feb 12 20:05 fly


      ❯ sudo chmod -R 0700 /usr/local/bin/fly


      ❯ ls -lah /usr/local/bin | grep fly

        drwx------   4 <user>  staff   128B Feb 12 20:05 fly


      ❯ open ~/.zshrc

        # tambahkan pada baris terakhir
        export PATH=$PATH:/usr/local/bin/fly/bin


      # apply perubahan
      ❯ source ~/.zshrc


      # check, find the section /usr/local/bin/fly/bin
      ❯ echo $PATH


## Sign Up

      ❯ flyctl auth signup

        Opening https://fly.io/app/auth/cli/8986bac405e4c52c88f218c776c8ea7f ...


        Waiting for session... Done
        successfully logged in as <your registered email>     