**Wireless network** is a computer network that uses wireless data connectionbetween network 
nodes.

# Terms

#### GSM

- Global System for Mobile Communication
- Generations: 2G (GSM), 3G (UMTS), 4G (LTE)
- Frequency: 900 MHz - 1800 MHz

#### Access Point

Access Point (AP) or Wireless Access Point (WAP) is a hardware device that allows wireless 
connectivity to the end devices.

#### Service Set Identifier (SSID)

- 32 bit identification string of the Access Point, the AP's name
- SSID inserted into the header of every data packet

#### Basic Service Set Identifier (BSSID)

- MAC address of the Access Point

#### ISM Band

A frequency band dedicated to the Industrial, Scientific and Medical purpose.

#### Wireless Standards

| Protocol  |  Frequency  | Modulation |
|:---------:|:-----------:|:----------:|
|  802.11a  |    5 GHz    |    OFDM    |
|  802.11b  |   2.4 GHz   |    DSSS    |		
|  802.11g  |   2.4 Ghz   |    OFDM    |
|  802.11n  |  2.4/5 Ghz  | MIMO-OFDM  |
|  802.11ac |    5 Ghz    | MIMO-OFDM  |
| Bluetooth |   2.4 Ghz   |

# Wi-FI 

Wi-Fi is a local area networking technology based on the IEEE 802.11 standard.

## Wi-Fi  Authentication

- Open authentication
- Shared Key authentication

### Open Authentication

|               Client               |    |                     WAP              |
|:----------------------------------:|:--:|:------------------------------------:|
|          Probe Request             | -> |                                      |
|                                    | <- |          Probe Response              |
| Open System Authentication Request | -> |                                      |
|                                    | <- |  Open System Authetication Response  |
|       Association Request          | -> |                                      |
|                                    | <- |      Association Response            | 

- The Probe Request is to discover the network
- The Probe Response contains the parameters (SSID, data rate, encryption, ...)
- The Open System Authentication Request (authentication frame) is to set authentication open, 
the sequence number is set to 0x0001
- The Open System Request Response's sequence number is 0x0002
- The Association Request contains the security parameters (choosen encryption, ...)
- The Association Response complete the assiciation process

### Shared Key Authentication

|               Client               |    |                       WAP                   |
|:----------------------------------:|:--:|:-------------------------------------------:|
|      Authentication Request        | -> |                                             |
|                                    | <- | Authentication Response with Challenge Text |
|   Encypted Challenge Response      | -> |                                             |
|                                    | <- |     Successful / Unseccessful response      |

**Challenge test** :

- The client encrypt the challenge test with his shared key
- The AP decrypt the encrypted challenge test with his shared key, if the decrypted text 
matches, the successful authentication response frame is sent to the client
- This challenge test can be captured by a hacker as a clear text, so the hacker can get the 
shared key

## IEEE 802.1X

IEEE 802.1X is an IEEE Standard for port-based Network Access Control (PNAC). It provides an authentication mechanism to devices 
wishing to attach to a LAN or WLAN.

Extensible Authentication Protocol (EAP) is an authentication framework frequently used in wireless networks and point-to-point 
connections. For example, in IEEE 802.11 (WiFi) the WPA and WPA2 standards have adopted IEEE 802.1X with one hundred EAP Types as 
the official authentication mechanisms.

#### Parties

- **Supplicant** : a client device (such as a laptop) that wishes to attach to the LAN/WLAN
- **Authenticator** : a network device, such as an Ethernet switch or wireless access point
- **Authentication server** : typically a host running software supporting the RADIUS and EAP protocols

#### Authentication Progress

1. The client may send an EAP-start message.
2. The access point sends an EAP-request identity message.
3. The client's EAP-response packet with the client's identity is "proxied" to the authentication server by the authenticator.
4. The authentication server challenges the client to prove themselves and may send its credentials to prove itself to the client 
(if using mutual authentication).
5. The client checks the server's credentials (if using mutual authentication) and then sends its credentials to the server to 
prove itself.
6. The authentication server accepts or rejects the client's request for connection.
7. If the end user was accepted, the authenticator changes the virtual port with the end user to an authorized state allowing full 
network access to that end user.
8. At log-off, the client virtual port is changed back to the unauthorized state.

## Wardriving

Wardriving is the act of searching for Wi-Fi wireless networks by a person usually in a moving vehicle, using a laptop or 
smartphone.

**Variants** : warwalking, warcycling, warflying (drone)

**Warchalking** is the drawing of [symbols](https://78.media.tumblr.com/tumblr_llnht1usC11qk3ul6o1_500.jpg) in public places to 
advertise Wi-Fi networks.

## Types of Wireless Antennas

#### Directional Antenna

Direction antennas are designed to function in a specific direction to improve efficiency

Some types of directional antenna: [Parabolic antenna](https://en.wikipedia.org/wiki/Parabolic_antenna) , [Yagi-Uda 
antenna](https://en.wikipedia.org/wiki/Yagi_antenna) , [Horn antenna](https://en.wikipedia.org/wiki/Horn_antenna)

#### Omnidirectional antennas

Omnidirectional antenna radiates equal radio power in all directions.
When graphed in three dimensions this radiation pattern is often described as doughnut-shaped.

Use cases: radio broadcating, cell phones, GPS

Some type: [Whip antenna](https://en.wikipedia.org/wiki/Whip_antenna) , [Rubber Ducky 
antenna](https://en.wikipedia.org/wiki/Rubber_Ducky_antenna) , [Monopole antenna](https://en.wikipedia.org/wiki/Monopole_antenna)

