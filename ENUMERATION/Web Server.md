
Visit `http://<MACHINE IP>/blog/`.


![[Screenshot from 2025-09-11 12-15-48.png]]


Take a look at the Page Source and you'll find it's powered by 

![[Screenshot from 2025-09-11 12-19-23.png]]

## Log in

There's a button to go to the log in page. ![[Screenshot from 2025-09-12 10-43-08.png]]

![[Screenshot from 2025-09-12 10-44-11.png]]

You don't have any credentials to log in.

## Forgot your password

Go to that page and try to  enumerate some account.

If a user is not in the system, we get the message "User not found".

![[Screenshot from 2025-09-12 10-52-52.png]]


If you introduce the `admin's` accoount.

![[Screenshot from 2025-09-12 10-50-14.png]]

Here, you can see, that the `admin` user is present, because of an error in SendMailMessage.

## Burp suite 

- Intercept this method with Burp Proxy.

- Send the query to "Intruder" to enumerate more users.
	 ![[Screenshot from 2025-09-12 10-59-35.png]]

- On Intruder Add `§admin§` to evaluate this position.
	 ![[Screenshot from 2025-09-12 11-10-18.png]]

- As wordlist use `/usr/share/seclists/Usernames/cirt-default-usernames.txt` from the packet.
	![[Screenshot from 2025-09-12 11-16-58.png]]

- Send the attack.
- After a while you'll get two users: admin and GUEST.
	![[Screenshot from 2025-09-12 11-30-13.png]]

	![[Screenshot from 2025-09-12 11-31-28.png]]

**Next step:** [[Decoding the URL and the users' hashes]]
