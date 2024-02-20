# Forensic Challenges

## Foremost

[Foremost](https://www.kali.org/tools/foremost/) is a tool for recovering files from memory dumps for example.
File types such as doc, jpg, pdf and xls can be extracted.

### Foremost usage

The tool can be used with command:

```shell
foremost -t doc,jpg,pdf -i <memory_image.dmp>
```
The output is given to output folder, where the results can be viewed.

***

## Exiftool

[Exiftool](https://github.com/exiftool/exiftool) can be used to investigate files metadata.

### Exiftool usage

The tool can be installed with command:
```bash
apt install exiftool
```

The tool can extract information with command:

```bash
exiftool <image.jpg>
```

***

## Volatility

[Volatility](https://github.com/volatilityfoundation/volatility) can be used to investigate memory dump files.

The binaries releases for Volatility2 and Volatility3 can be found from [here](https://www.volatilityfoundation.org/releases)

### Volatility usage

List all processes from a Windows machine with Volatility3:
```bash
python3 volatility3/vol.py <memory_dump.dmp> windows.pslist.PsList > output/pslist.out
```

Take memdump with version 2 of Volatility:

```bash
./volatility_2.6_lin64_standalone/volatility_2.6_lin64_standalone -f <memdump.dmp> --profile=<machine_profile_here> memdump -p <pid_from_pslist> --dump-dir output/
```
Then make it readable with strings:

```bash
output/<pid.dmp> > output/<filename.out>
```

Grep for specific strings from dump file:

```bash
strings output/<pid_file>.dmp | grep "some specific string here" > output/specific_string.out
```

***

## Tcpdump

Tcpdump could be used to monitor active traffic from a server.

### Tcpdump usage

Monitor interface:
```bash
tcpdump -i <interface_here>
```
Monitor output in ASCII:
```bash
tcpdump -A -i <interface>
```

***

## Wireshark

Wireshark can be used to investigate *.pcap files.
Often capture files contain information about network or serial or bluetooth activity.
For aiding investigations, it is often useful to track the specific trace.
