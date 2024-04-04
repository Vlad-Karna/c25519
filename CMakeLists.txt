cmake_minimum_required(VERSION 3.0)

project(c25519)

set(SRC
	c25519.c	c25519.h
	ed25519.c	ed25519.h
	edsign.c	edsign.h
	f25519.c	f25519.h
	fprime.c	fprime.h
	morph25519.c	morph25519.h
	sha512.c	sha512.h
)

list(TRANSFORM SRC PREPEND src/)

add_library(${PROJECT_NAME} ${SRC})

target_include_directories(${PROJECT_NAME} PUBLIC src)
