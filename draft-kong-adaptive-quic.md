---
title: "An adaptive transport protocol based on quic to cater to certain environment and business"
abbrev: Adaptive-QUIC
docname: draft-kong-adaptive-quic-00
date: {DATE}
category: std
ipr: trust200902
area: Transport
workgroup: QUIC

stand_alone: yes
pi: [toc, sortrefs, symrefs, docmapping]

author:
  -
    ins: t. kong
    name: Lingtao Kong
    org: AntFin.
    email: itkltao@sina.com

normative:

  TIME_T:
    title: "Open Group Standard: Vol. 1: Base Definitions, Issue 7"
    date: 2018
    seriesinfo: IEEE Std 1003.1
    target: http://pubs.opengroup.org/onlinepubs/9699919799/basedefs/V1_chap04.html#tag_04_16

--- abstract

adaptive quic ...

--- middle

# Introduction

adaptive quic is ...

## Terminology

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD",
"SHOULD NOT", "RECOMMENDED", "MAY", and "OPTIONAL" in this document are to be
interpreted as described in RFC 2119 {{?RFC2119}}.

In this document, these words will appear with that interpretation only when in
ALL CAPS.  Lower case uses of these words are not to be interpreted as carrying
significance described in RFC 2119.

In this document, "client" and "server" refer to the endpoints of a QUIC
connection unless otherwise indicated.  A "load balancer" is an intermediary for
that connection that does not possess QUIC connection keys, but it may rewrite
IP addresses or conduct other IP or UDP processing. A "configuration agent" is
the entity that determines the QUIC-LB configuration parameters for the network
and leverages some system to distribute that configuration.

Note that stateful load balancers that act as proxies, by terminating a QUIC
connection with the client and then retrieving data from the server using QUIC
or another protocol, are treated as a server with respect to this specification.

For brevity, "Connection ID" will often be abbreviated as "CID".

## Notation

All wire formats will be depicted using the notation defined in Section 1.3 of
{{QUIC-TRANSPORT}}. There is one addition: the function len() refers to the
length of a field which can serve as a limit on a different field, so that the
lengths of two fields can be concisely defined as limited to a sum, for example:

x(A..B)
y(C..B-len(x))

indicates that x can be of any length between A and B, and y can be of any
length between C and B provided that (len(x) + len(y)) does not exceed B.

The example below illustrates the basic framework:

~~~
Example Structure {
  One-bit Field (1),
  7-bit Field with Fixed Value (7) = 61,
  Field with Variable-Length Integer (i),
  Arbitrary-Length Field (..),
  Variable-Length Field (8..24),
  Variable-Length Field with Dynamic Limit (8..24-len(Variable-Length Field)),
  Field With Minimum Length (16..),
  Field With Maximum Length (..128),
  [Optional Field (64)],
  Repeated Field (8) ...,
}
~~~
{: #fig-ex-format title="Example Format"}

# Protocol Objectives

## Simplicity

adaptive quic 

## Security

adaptive quic



# Security Considerations {#security-considerations}

Adaptive-QUIC is 

## xxx


# IANA Considerations

There are no IANA requirements.

--- back




# Acknowledgments

balabala

# Change Log

balabala


