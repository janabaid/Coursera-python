# Coursera-python
#Just for testing 
# Use the file name mbox-short.txt as the file name
fname = input("Enter file name: ")
fh = open(fname)

count = 0
avg = 0
for line in fh:
    if not line.startswith("X-DSPAM-Confidence:"): continue
    # print(line)
    pos = line.find(" ")
    val = line[pos:].rstrip()
    # print(val)
    val = float(val)
    count = count + 1
    # print(count)
    avg = avg + val
print("Average spam confidence: ", avg / count)
