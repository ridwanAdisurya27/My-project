``` mermaid
graph LR
    subgraph features
    direction LR
        features_1[brush on canvas]
        features_2[mengganti warna]
        features_3[mengubah ukuran brush]
        features_4[mengganti layer]
        features_5[save image]
    end
    subgraph variabel
    direction LR
        warna
        size
    end
        %% f1_features algo
        f1_algo1[initialise canvas]
        f1_algo2[warnai block dengan warna yang dipilih user]
        f1_algo3([end])
        features_1 --> f1_algo1
        f1_algo1 --user klik block--> f1_algo2
        f1_algo2 --> f1_algo3
        warna --send color--> f1_algo2
        %% f2_fatures algo
        f2_algo1[show RGB Picker]
        features_2 --> f2_algo1
        f2_algo1 --change--> warna
        %% f3_features algo
        f3_algo1[/show slider input dengan nilai 1-10/]
        features_3 --user klik icon size-->f3_algo1
        f3_algo1 --change-->size
        size --> f1_algo2

