import subprocess
import logging
import multiprocessing
import time

logging.basicConfig(filename='./ping.log',level=logging.DEBUG)


def checkIP(text, firstOct):
    logging.basicConfig(filename='./ping' + firstOct + '.log', level=logging.DEBUG)

    IP = text
    ping_command = "ping -c 1 -n -W 1 " + IP

    (output, error) = subprocess.Popen(ping_command,
                                   stdout=subprocess.PIPE,
                                   stderr=subprocess.PIPE,
                                   shell=True).communicate()
    logging.info("###" + text + "###,")
    logging.info(str(output) + str(error))
    print(output, error)

def checkWrapper(text):
    firstOct = text
    for x in range(0, 999):
        for y in range(0, 999):
            for z in range(0, 999):
                checkIP(text + str(x) + "." + str(y) + "." + str(z), firstOct)




def mp_worker(textWorker):
    print(" Processs Starting: " + textWorker)
    checkWrapper(textWorker)
    print(" Process Stopping: " + textWorker)

def mp_handler():
    p = multiprocessing.Pool(12)
    p.map(mp_worker, data)

if __name__ == '__main__':
    data = list()
    for x in range(0, 999):
        data.append(str(x) + ".")
        print(str(x) + ".")
    mp_handler()
