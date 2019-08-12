cmake_minimum_required(VERSION 2.8)
project(marisa)
add_library(marisa STATIC
	marisa/agent.cc
	marisa/grimoire/io/mapper.cc
	marisa/grimoire/io/reader.cc
	marisa/grimoire/io/writer.cc
	marisa/grimoire/trie/louds-trie.cc
	marisa/grimoire/trie/tail.cc
	marisa/grimoire/vector/bit-vector.cc
	marisa/keyset.cc
	marisa/trie.cc

)

target_include_directories(marisa PUBLIC . ../include)
