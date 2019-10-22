
ifeq ($(RTE_SDK),)
$(error "Please define RTE_SDK environment variable")
endif

# Default target, can be overriden by command line or environment
RTE_TARGET ?= x86_64-native-linuxapp-gcc

include $(RTE_SDK)/mk/rte.vars.mk

# lib name
LIB = liblwip.a

# all source are stored in SRCS-y
SRCS-y := altcp_alloc.c
SRCS-y += altcp.c
SRCS-y += altcp_tcp.c
SRCS-y += def.c
SRCS-y += dns.c
SRCS-y += inet_chksum.c
SRCS-y += init.c
SRCS-y += ip.c

# IPV4 sources
SRCS-y += ipv4/autoip.c
SRCS-y += ipv4/dhcp.c
SRCS-y += ipv4/etharp.c
SRCS-y += ipv4/icmp.c
SRCS-y += ipv4/igmp.c
SRCS-y += ipv4/ip4_addr.c
SRCS-y += ipv4/ip4.c
SRCS-y += ipv4/ip4_frag.c

# IPV6 sources
SRCS-y += ipv6/dhcp6.c
SRCS-y += ipv6/ethip6.c
SRCS-y += ipv6/icmp6.c
SRCS-y += ipv6/inet6.c
SRCS-y += ipv6/ip6_addr.c
SRCS-y += ipv6/ip6.c
SRCS-y += ipv6/ip6_frag.c
SRCS-y += ipv6/mld6.c
SRCS-y += ipv6/nd6.c

SRCS-y += mem.c
SRCS-y += memp.c
SRCS-y += netif.c
SRCS-y += pbuf.c
SRCS-y += raw.c
SRCS-y += stats.c
SRCS-y += sys.c
SRCS-y += tcp.c
SRCS-y += tcp_in.c
SRCS-y += tcp_out.c
SRCS-y += timeouts.c
SRCS-y += udp.c

CFLAGS += -O0 -g
CFLAGS += -I../../include

include $(RTE_SDK)/mk/rte.extlib.mk

