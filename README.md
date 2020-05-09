# utl-untransposing-several-variables-into-name-value-pairs
Untransposing several variables into name value pairs
    Untransposing several variables into name value pairs                                                             
                                                                                                                      
    github                                                                                                            
    https://tinyurl.com/y89jd357                                                                                      
    https://github.com/rogerjdeangelis/utl-untransposing-several-variables-into-name-value-pairs                      
                                                                                                                      
      Two Solutions                                                                                                   
            a. Untranspose macro  (http://tiny.cc/untranspose_macro)                                                  
            b. gather macro (Alea Iacta  https://github.com/clindocu)                                                 
                                                                                                                      
    SAS Forum                                                                                                         
    https://tinyurl.com/ybbh49xc                                                                                      
    https://communities.sas.com/t5/SAS-Programming/Structure-change/m-p/646012                                        
                                                                                                                      
    macros                                                                                                            
    https://tinyurl.com/y9nfugth                                                                                      
    https://github.com/rogerjdeangelis/utl-macros-used-in-many-of-rogerjdeangelis-repositories                        
                                                                                                                      
                                                                                                                      
    *_                   _                                                                                            
    (_)_ __  _ __  _   _| |_                                                                                          
    | | '_ \| '_ \| | | | __|                                                                                         
    | | | | | |_) | |_| | |_                                                                                          
    |_|_| |_| .__/ \__,_|\__|                                                                                         
            |_|                                                                                                       
    ;                                                                                                                 
                                                                                                                      
    DATA WORK.have;                                                                                                   
        INPUT                                                                                                         
            LocID                                                                                                     
            Number                                                                                                    
            Pct_HpA                                                                                                   
            Pct_Bh                                                                                                    
            Pct_Menin                                                                                                 
            Pct_Rot                                                                                                   
            Pct_Ap                                                                                                    
            yr          ;                                                                                             
    cards44;                                                                                                          
    1 21876 89.4 94.7 94.3 96.6 98.2 20082009                                                                         
    1 21876 289.4 294.7 294.3 296.6 298.2 20082009                                                                    
    2 2135 94.8 100 99.2 99.3 100 20082009                                                                            
    3 2449 90.5 96.3 95.5 98.1 98.8 20082009                                                                          
    4 4754 89.1 94.6 93.9 97.4 98.2 20082009                                                                          
    5 2529 81.7 87.2 89.3 95.4 95.8 20082009                                                                          
    1 21556 87.1 92.1 93.3 94.1 95.7 20092010                                                                         
    2 2142 89.5 94.7 93.9 94 94.7 20092010                                                                            
    3 2408 93.4 98.6 97.4 99.3 100 20092010                                                                           
    4 4786 91 95.8 94.7 97.2 98.4 20092010                                                                            
    5 2527 85.6 91.6 90.8 97.3 98.3 20092010                                                                          
    1 21708 88.3 94.3 93.5 95.3 97.2 20102011                                                                         
    2 2135 86.5 91.7 90.9 91 91.7 20102011                                                                            
    3 2419 88.7 94.3 91.4 95.9 98.3 20102011                                                                          
    4 4825 90.4 95.8 94.2 97.2 98.2 20102011                                                                          
    5 2575 84.6 91.6 88.1 94.9 97.6 20102011                                                                          
    ;;;;                                                                                                              
    run;                                                                                                              
                                                                                                                      
                                                                                                                      
     WORK.HAVE total obs=16        RULE (create name value pairs by locid number yr)                                  
                                                                                                                      
                                                         PCT                                                          
      LOCID    NUMBER      YR      PCT_HPA    PCT_BH    MENIN    PCT_ROT    PCT_AP                                    
                                                                                                                      
        1       21876   20082009     89.4       94.7     94.3      96.6       98.2                                    
        1       21876   20082009    289.4      294.7    294.3     296.6      298.2                                    
                                                                                                                      
        2        2135   20082009     94.8      100.0     99.2      99.3      100.0                                    
        3        2449   20082009     90.5       96.3     95.5      98.1       98.8                                    
        4        4754   20082009     89.1       94.6     93.9      97.4       98.2                                    
        5        2529   20082009     81.7       87.2     89.3      95.4       95.8                                    
        1       21556   20092010     87.1       92.1     93.3      94.1       95.7                                    
        2        2142   20092010     89.5       94.7     93.9      94.0       94.7                                    
        3        2408   20092010     93.4       98.6     97.4      99.3      100.0                                    
        4        4786   20092010     91.0       95.8     94.7      97.2       98.4                                    
        5        2527   20092010     85.6       91.6     90.8      97.3       98.3                                    
        1       21708   20102011     88.3       94.3     93.5      95.3       97.2                                    
        2        2135   20102011     86.5       91.7     90.9      91.0       91.7                                    
        3        2419   20102011     88.7       94.3     91.4      95.9       98.3                                    
        4        4825   20102011     90.4       95.8     94.2      97.2       98.2                                    
        5        2575   20102011     84.6       91.6     88.1      94.9       97.6                                    
                                                                                                                      
    *            _               _                                                                                    
      ___  _   _| |_ _ __  _   _| |_                                                                                  
     / _ \| | | | __| '_ \| | | | __|                                                                                 
    | (_) | |_| | |_| |_) | |_| | |_                                                                                  
     \___/ \__,_|\__| .__/ \__,_|\__|                                                                                 
                    |_|    _                                                                                          
      __ _     _   _ _ __ | |_ _ __ __ _ _ __  ___ _ __   ___  ___  ___                                               
     / _` |   | | | | '_ \| __| '__/ _` | '_ \/ __| '_ \ / _ \/ __|/ _ \                                              
    | (_| |_  | |_| | | | | |_| | | (_| | | | \__ \ |_) | (_) \__ \  __/                                              
     \__,_(_)  \__,_|_| |_|\__|_|  \__,_|_| |_|___/ .__/ \___/|___/\___|                                              
                                                  |_|                                                                 
    ;                                                                                                                 
                                                                                                                      
                                     NAME VALUE PAIRS                                                                 
    WORK.WANT total obs=80           =================                                                                
                                                                                                                      
      LOCID    NUMBER       YR       NAMES     PCT                                                                    
                                                                                                                      
        1       21876    20082009    HPA       89.4                                                                   
        1       21876    20082009    BH        94.7                                                                   
        1       21876    20082009    MENIN     94.3                                                                   
        1       21876    20082009    ROT       96.6                                                                   
        1       21876    20082009    AP        98.2                                                                   
        1       21876    20082009    HPA      289.4                                                                   
        1       21876    20082009    BH       294.7                                                                   
        1       21876    20082009    MENIN    294.3                                                                   
        1       21876    20082009    ROT      296.6                                                                   
        1       21876    20082009    AP       298.2                                                                   
                                                                                                                      
        2        2135    20082009    HPA       94.8                                                                   
        2        2135    20082009    BH       100.0                                                                   
        2        2135    20082009    MENIN     99.2                                                                   
        2        2135    20082009    ROT       99.3                                                                   
        2        2135    20082009    AP       100.0                                                                   
                                                                                                                      
        3        2449    20082009    HPA       90.5                                                                   
        3        2449    20082009    BH        96.3                                                                   
        3        2449    20082009    MENIN     95.5                                                                   
        3        2449    20082009    ROT       98.1                                                                   
        3        2449    20082009    AP        98.8                                                                   
                                                                                                                      
    ...                                                                                                               
                                                                                                                      
    *_                    _   _                                                                                       
    | |__      __ _  __ _| |_| |__   ___ _ __                                                                         
    | '_ \    / _` |/ _` | __| '_ \ / _ \ '__|                                                                        
    | |_) |  | (_| | (_| | |_| | | |  __/ |                                                                           
    |_.__(_)  \__, |\__,_|\__|_| |_|\___|_|                                                                           
              |___/                                                                                                   
    ;                                                                                                                 
    WORK.WANT total obs=80                                                                                            
                                                                                                                      
       LOCID    NUMBER       YR       NAM           VAL                                                               
                                                                                                                      
         1       21876    20082009    PCT_HPA       89.4                                                              
         1       21876    20082009    PCT_BH        94.7                                                              
         1       21876    20082009    PCT_MENIN     94.3                                                              
         1       21876    20082009    PCT_ROT       96.6                                                              
         1       21876    20082009    PCT_AP        98.2                                                              
         1       21876    20082009    PCT_HPA      289.4                                                              
         1       21876    20082009    PCT_BH       294.7                                                              
         1       21876    20082009    PCT_MENIN    294.3                                                              
         1       21876    20082009    PCT_ROT      296.6                                                              
         1       21876    20082009    PCT_AP       298.2                                                              
                                                                                                                      
         2        2135    20082009    PCT_HPA       94.8                                                              
         2        2135    20082009    PCT_BH       100.0                                                              
         2        2135    20082009    PCT_MENIN     99.2                                                              
         2        2135    20082009    PCT_ROT       99.3                                                              
         2        2135    20082009    PCT_AP       100.0                                                              
                                                                                                                      
         3        2449    20082009    PCT_HPA       90.5                                                              
         3        2449    20082009    PCT_BH        96.3                                                              
         3        2449    20082009    PCT_MENIN     95.5                                                              
         3        2449    20082009    PCT_ROT       98.1                                                              
         3        2449    20082009    PCT_AP        98.8                                                              
         4        4754    20082009    PCT_HPA       89.1                                                              
         4        4754    20082009    PCT_BH        94.6                                                              
         4        4754    20082009    PCT_MENIN     93.9                                                              
         4        4754    20082009    PCT_ROT       97.4                                                              
         4        4754    20082009    PCT_AP        98.2                                                              
         5        2529    20082009    PCT_HPA       81.7                                                              
         5        2529    20082009    PCT_BH        87.2                                                              
         5        2529    20082009    PCT_MENIN     89.3                                                              
         5        2529    20082009    PCT_ROT       95.4                                                              
         5        2529    20082009    PCT_AP        95.8                                                              
         1       21556    20092010    PCT_HPA       87.1                                                              
         1       21556    20092010    PCT_BH        92.1                                                              
         1       21556    20092010    PCT_MENIN     93.3                                                              
         1       21556    20092010    PCT_ROT       94.1                                                              
         1       21556    20092010    PCT_AP        95.7                                                              
         2        2142    20092010    PCT_HPA       89.5                                                              
         2        2142    20092010    PCT_BH        94.7                                                              
         2        2142    20092010    PCT_MENIN     93.9                                                              
         2        2142    20092010    PCT_ROT       94.0                                                              
         2        2142    20092010    PCT_AP        94.7                                                              
                                                                                                                      
    *          _       _   _                                                                                          
     ___  ___ | |_   _| |_(_) ___  _ __  ___                                                                          
    / __|/ _ \| | | | | __| |/ _ \| '_ \/ __|                                                                         
    \__ \ (_) | | |_| | |_| | (_) | | | \__ \                                                                         
    |___/\___/|_|\__,_|\__|_|\___/|_| |_|___/                                                                         
                           _                                                                                          
      __ _     _   _ _ __ | |_ _ __ __ _ _ __  ___ _ __   ___  ___  ___                                               
     / _` |   | | | | '_ \| __| '__/ _` | '_ \/ __| '_ \ / _ \/ __|/ _ \                                              
    | (_| |_  | |_| | | | | |_| | | (_| | | | \__ \ |_) | (_) \__ \  __/                                              
     \__,_(_)  \__,_|_| |_|\__|_|  \__,_|_| |_|___/ .__/ \___/|___/\___|                                              
                                                  |_|                                                                 
    ;                                                                                                                 
    * Macro;                                                                                                          
    filename ut url 'http://tiny.cc/untranspose_macro';                                                               
    %include ut ;                                                                                                     
                                                                                                                      
    %untranspose(                                                                                                     
       data=have                                                                                                      
      ,out=want(rename=(_name_=names _value_=pct))                                                                    
      ,by=locid number yr                                                                                             
      ,prefix=Pct_                                                                                                    
      ,var=HpA Bh Menin Rot Ap                                                                                        
    );                                                                                                                
                                                                                                                      
    *_                    _   _                                                                                       
    | |__      __ _  __ _| |_| |__   ___ _ __                                                                         
    | '_ \    / _` |/ _` | __| '_ \ / _ \ '__|                                                                        
    | |_) |  | (_| | (_| | |_| | | |  __/ |                                                                           
    |_.__(_)  \__, |\__,_|\__|_| |_|\___|_|                                                                           
              |___/                                                                                                   
    ;                                                                                                                 
                                                                                                                      
    %utl_gather(have, nam, Val, locid number yr, want, ValFormat=8.1);                                                
                                                                                                                      
                                                                                                                      
