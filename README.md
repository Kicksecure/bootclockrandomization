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

1\. Add [Whonix's Signing Key](https://www.whonix.org/wiki/Whonix_Signing_Key).

```
sudo apt-key --keyring /etc/apt/trusted.gpg.d/whonix.gpg adv --keyserver hkp://ipv4.pool.sks-keyservers.net:80 --recv-keys 916B8D99C38EAF5E8ADC7A2A8D66066A2EEACCDA
```

3\. Add Whonix's APT repository.

```
echo "deb http://deb.whonix.org buster main" | sudo tee /etc/apt/sources.list.d/whonix.list
```

4\. Update your package lists.

```
sudo apt-get update
```

5\. Install `bootclockrandomization`.

```
sudo apt-get install bootclockrandomization
```

## How to Build deb Package ##

Replace `apparmor-profile-torbrowser` with the actual name of this package with `bootclockrandomization` and see [instructions](https://www.whonix.org/wiki/Dev/Build_Documentation/apparmor-profile-torbrowser).

## Contact ##

* [Free Forum Support](https://forums.whonix.org)
* [Professional Support](https://www.whonix.org/wiki/Professional_Support)

## Payments ##

`bootclockrandomization` requires [payments](https://www.whonix.org/wiki/Payments) to stay alive!
