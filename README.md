# Poke CCSDS
poke-ccsds is a [GNU poke](https://www.jemarch.net/poke) pickle for analyzing
CCSDS protocols.

## Supported Protocols

* Space Packet Protocol
* Encapsulation Packet Protocol
* TM Space Data Link Protocol
* TC Space Data Link Protocol
* AOS Space Data Link Protocol
* Unified Space Data Link Protocol
* Space Data Link Security Protocol

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

### USLP
`uslp_insert_zone_length`: USLP insert zone length, 0 for not present.

`uslp_frame_length`:AOS transfer frame length.

`uslp_ocf_present`: Bit indicating the presence of the operational control
field.

`uslp_fecf_present`: Bit indicating the presence of the frame error control
field.


### SDLS
`sdls_iv_length`: IV field length.

`sdls_seq_length`: Sequence number field length.

`sdls_pad_len_length`: Pad length field length.

`sdls_mac_length`: Message authentication code length.
