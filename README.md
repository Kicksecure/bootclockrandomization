# Randomizes clock when systems boots #

Randomizes clock at boot time. Moves clock a few seconds and nanoseconds
to past or future. Useful in context of anonymity/privacy/Tor.

This is useful to enforce the design goal, that the host clock and
Gateway/Workstation clock should always slightly differ (even before secure
timesync succeeded!) to prevent time based fingerprinting / linkablity
issues.

Runs before Tor / sdwdate (if installed).

See also: https://www.whonix.org/wiki/Dev/TimeSync

## How to install `bootclockrandomization` using apt-get ##

1\. Download the APT Signing Key.

```
wget https://www.kicksecure.com/keys/derivative.asc
```

Users can [check the Signing Key](https://www.kicksecure.com/wiki/Signing_Key) for better security.

2\. Add the APT Signing Key.

```
sudo cp ~/derivative.asc /usr/share/keyrings/derivative.asc
```

3\. Add the derivative repository.

```
echo "deb [signed-by=/usr/share/keyrings/derivative.asc] https://deb.kicksecure.com trixie main contrib non-free" | sudo tee /etc/apt/sources.list.d/derivative.list
```

4\. Update your package lists.

```
sudo apt-get update
```

5\. Install `bootclockrandomization`.

```
sudo apt-get install bootclockrandomization
```

## How to Build deb Package from Source Code ##

Can be build using standard Debian package build tools such as:

```
dpkg-buildpackage -b
```

See instructions.

NOTE: Replace `generic-package` with the actual name of this package `bootclockrandomization`.

* **A)** [easy](https://www.kicksecure.com/wiki/Dev/Build_Documentation/generic-package/easy), _OR_
* **B)** [including verifying software signatures](https://www.kicksecure.com/wiki/Dev/Build_Documentation/generic-package)

## Contact ##

* [Free Forum Support](https://forums.kicksecure.com)
* [Premium Support](https://www.kicksecure.com/wiki/Premium_Support)

## Donate ##

`bootclockrandomization` requires [donations](https://www.kicksecure.com/wiki/Donate) to stay alive!
