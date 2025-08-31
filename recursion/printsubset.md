graph TD
    A0["Index=0, Subset=[]"]
    A1["Include 1 -> [1]"]
    A2["Include 2 -> [1,2]"]
    A3["Include 3 -> [1,2,3] -> Add to result"]
    A4["Exclude 3 -> [1,2] -> Add to result"]
    A5["Exclude 2 -> [1]"]
    A6["Include 3 -> [1,3] -> Add to result"]
    A7["Exclude 3 -> [1] -> Add to result"]
    B1["Exclude 1 -> []"]
    B2["Include 2 -> [2]"]
    B3["Include 3 -> [2,3] -> Add to result"]
    B4["Exclude 3 -> [2] -> Add to result"]
    B5["Exclude 2 -> []"]
    B6["Include 3 -> [3] -> Add to result"]
    B7["Exclude 3 -> [] -> Add to result"]

    A0 --> A1 --> A2 --> A3
    A2 --> A4
    A1 --> A5 --> A6
    A5 --> A7
    A0 --> B1 --> B2 --> B3
    B2 --> B4
    B1 --> B5 --> B6
    B5 --> B7
