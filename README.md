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

1\. Download [Whonix's Signing Key]().

```
wget https://www.whonix.org/patrick.asc
```

Users can [check Whonix Signing Key](https://www.whonix.org/wiki/Whonix_Signing_Key) for better security.

2\. Add Whonix's signing key.

```
sudo apt-key --keyring /etc/apt/trusted.gpg.d/whonix.gpg add ~/patrick.asc
```

3\. Add Whonix's APT repository.

```
echo "deb https://deb.whonix.org buster main contrib non-free" | sudo tee /etc/apt/sources.list.d/whonix.list
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

See [instructions](https://www.whonix.org/wiki/Dev/Build_Documentation/bootclockrandomization). (Replace `package-name` with the actual name of this package.)

## Contact ##

* [Free Forum Support](https://forums.whonix.org)
* [Professional Support](https://www.whonix.org/wiki/Professional_Support)

## Donate ##

`bootclockrandomization` requires [donations](https://www.whonix.org/wiki/Donate) to stay alive!
