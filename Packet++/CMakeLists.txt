cmake_minimum_required(VERSION 3.0)

add_library(PacketPP
	src/ArpLayer.cpp
	src/BgpLayer.cpp
	src/DhcpLayer.cpp
	src/DhcpV6Layer.cpp
	src/DnsLayer.cpp
	src/DnsResource.cpp
	src/DnsResourceData.cpp
	src/EthDot3Layer.cpp
	src/EthLayer.cpp
	src/FtpLayer.cpp
	src/GreLayer.cpp
	src/GtpLayer.cpp
	src/HttpLayer.cpp
	src/IcmpLayer.cpp
	src/IgmpLayer.cpp
	src/IPReassembly.cpp
	src/IPSecLayer.cpp
	src/IPv4Layer.cpp
	src/IPv6Extensions.cpp
	src/IPv6Layer.cpp
	src/Layer.cpp
	src/MplsLayer.cpp
	src/NtpLayer.cpp
	src/NullLoopbackLayer.cpp
	src/Packet.cpp
	src/PacketTrailerLayer.cpp
	src/PacketUtils.cpp
	src/PayloadLayer.cpp
	src/PPPoELayer.cpp
	src/RadiusLayer.cpp
	src/RawPacket.cpp
	src/SdpLayer.cpp
	src/SingleCommandTextProtocol.cpp
	src/SipLayer.cpp
	src/SllLayer.cpp
	src/SSHLayer.cpp
	src/SSLCommon.cpp
	src/SSLHandshake.cpp
	src/SSLLayer.cpp
	src/TcpLayer.cpp
	src/TcpReassembly.cpp
	src/TelnetLayer.cpp
	src/TextBasedProtocol.cpp
	src/TLVData.cpp
	src/UdpLayer.cpp
	src/VlanLayer.cpp
	src/VxlanLayer.cpp

	header/ArpLayer.h
	header/BgpLayer.h
	header/DhcpLayer.h
	header/DhcpV6Layer.h
	header/DnsLayer.h
	header/DnsResource.h
	header/DnsResourceData.h
	header/EthDot3Layer.h
	header/EthLayer.h
	header/FtpLayer.h
	header/GreLayer.h
	header/GtpLayer.h
	header/HttpLayer.h
	header/IcmpLayer.h
	header/IgmpLayer.h
	header/IPReassembly.h
	header/IPSecLayer.h
	header/IPv4Layer.h
	header/IPv6Extensions.h
	header/IPv6Layer.h
	header/Layer.h
	header/MplsLayer.h
	header/NtpLayer.h
	header/NullLoopbackLayer.h
	header/Packet.h
	header/PacketTrailerLayer.h
	header/PacketUtils.h
	header/PayloadLayer.h
	header/PPPoELayer.h
	header/RadiusLayer.h
	header/RawPacket.h
	header/SdpLayer.h
	header/SingleCommandTextProtocol.h
	header/SipLayer.h
	header/SllLayer.h
	header/SSHLayer.h
	header/SSLCommon.h
	header/SSLHandshake.h
	header/SSLLayer.h
	header/TcpLayer.h
	header/TcpReassembly.h
	header/TelnetLayer.h
	header/TextBasedProtocol.h
	header/TLVData.h
	header/UdpLayer.h
	header/VlanLayer.h
	header/VxlanLayer.h
)

target_include_directories(PacketPP
	PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/header
)

target_link_libraries(PacketPP PUBLIC
	CommonPP
	EndianPortable

)

set_property(TARGET PacketPP PROPERTY CXX_STANDARD 11)
set_property(TARGET PacketPP PROPERTY CXX_EXTENSIONS OFF)
set_property(TARGET PacketPP PROPERTY ARCHIVE_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/lib")
set_property(TARGET PacketPP PROPERTY OUTPUT_NAME "Packet++")
