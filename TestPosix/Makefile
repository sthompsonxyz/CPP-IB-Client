CXX=g++
CXXFLAGS=-DIB_USE_STD_STRING -Wall -Wno-switch -g
ROOT_DIR=../..
BASE_SRC_DIR=${ROOT_DIR}/source/PosixClient/src
INCLUDES=-I${ROOT_DIR}/source/PosixClient/Shared/ -I${BASE_SRC_DIR}
TARGET=PosixSocketClientTest

$(TARGET):
	$(CXX) $(CXXFLAGS) $(INCLUDES) -o EClientSocketBase.o -c $(BASE_SRC_DIR)/EClientSocketBase.cpp
	$(CXX) $(CXXFLAGS) $(INCLUDES) -o EPosixClientSocket.o -c $(BASE_SRC_DIR)/EPosixClientSocket.cpp
	$(CXX) $(CXXFLAGS) $(INCLUDES) -o PosixTestClient.o -c PosixTestClient.cpp
	$(CXX) $(CXXFLAGS) $(INCLUDES) -o Main.o -c Main.cpp
	$(CXX) $(CXXFLAGS) $(INCLUDES) -o $@ EClientSocketBase.o EPosixClientSocket.o PosixTestClient.o Main.o

clean:
	rm -f $(TARGET) *.o

