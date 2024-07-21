# Poke CCSDS
poke-ccsds is a [GNU poke](https://www.jemarch.net/poke) pickle for analyzing
CCSDS protocols.

## Supported Protocols

* Space Packet
* Encapsulation Packet
* TM Space Data Link
* TC Space Data Link
* AOS Space Data Link

## Managed Parameters
Many CCSDS protocols include "managed parameters" which affect the structure of
the frames.  These parameters must be configured after loading the pickle.

### TC
`tc_fecf_present`: Bit indicating the presence of the frame error control field.

### TM
`tm_frame_length`: TM transfer frame length.

`tm_fecf_present`: Bit indicating the presence of the frame error control field.

### AOS
`aos_fhec_present`: Bit indicating the presence of the frame header error
control field.

`aos_insert_zone_length`: AOS insert zone length, 0 for not present.

`aos_frame_length`: AOS transfer frame length.

`aos_fecf_present`: Bit indicating the presence of the frame error control
field.

`aos_ocf_present`: Array of bits indicating the presence of the operational
control field for each virtual channel.
