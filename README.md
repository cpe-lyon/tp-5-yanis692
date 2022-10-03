# tp-5-yanis692
tp-5-yanis692 created by GitHub Classroom

# Exerice 1

2. On affiche les differents disques dur et partitions avec 
```
ll /dev/sd*
```
![image](https://user-images.githubusercontent.com/77662970/193530068-8266ac93-e0ea-4811-b756-e1051ac6a4ab.png)

2. 

![image](https://user-images.githubusercontent.com/77662970/193533220-22af50ef-0006-4ce7-8eb1-ca7bc4ea7eb8.png)


![image](https://user-images.githubusercontent.com/77662970/193533096-6897c376-5da9-4d5c-be12-348e9d22153f.png)

3.
La commande pour accorder une partitions de fichier pour linux est 
```
sudo mkfs.ext4 /dev/sdb1
```

![image](https://user-images.githubusercontent.com/77662970/193534260-15fbb1be-53a7-46ea-9750-28eb16e3af33.png)

Pour NFTS /
```
sudo mkfs.ntfs /dev/sdb2
```

![image](https://user-images.githubusercontent.com/77662970/193535067-ac83e23a-6ee8-4ca8-aa3e-ca2e0573dea9.png)

4. La commande ```df -T``` ne marche pas sur nos 2 partitions car celle-ci ne sont pas encore montées.

5.
On doit modifier le fichier fstab
```
sudo nano /etc/fstab
```
puis on rentre les les lignes suivantes :

![image](https://user-images.githubusercontent.com/77662970/193541499-c253880f-3b18-4cbd-bcae-b2a0af1da647.png)

puis on redemarre la vm et on force la prise en compte des modification du fichier ```/fstab``` avec ```sudo mount -a```

# Exercice 2

1.
![image](https://user-images.githubusercontent.com/77662970/193544943-b800e0b9-351c-44fe-a99c-ce1e7728a2c6.png)

2.

![image](https://user-images.githubusercontent.com/77662970/193547876-3877cf67-d3ba-4cfe-8cef-2418286d24ad.png)

3.
```sudo pvcreate /dev/sdb1```
```sudo pvdisplay```

![image](https://user-images.githubusercontent.com/77662970/193549152-e793449d-8f9f-4173-ade9-e3fe77c1dc70.png)

4.

![image](https://user-images.githubusercontent.com/77662970/193559639-02d76c97-5951-465d-bea7-6558db1172fc.png)

5.
```
sudo lvcreate -n lvData -l 100%FREE grp1
```

6.

![image](https://user-images.githubusercontent.com/77662970/193569546-acb1a8fa-b16d-4ab1-99ef-11db5d5f2df7.png)

