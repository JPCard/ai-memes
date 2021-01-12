
1)
git lfs -> para descargar archivos grandes de git


git checkout .
git lfs pull -> descarga los archivos grandes 
git lfs fetch -> comando para hacer descarga efectiva de objetos lfs


2)
json de memes van en ai-memes/net/data/ImgFlip500K_Dataset

3) en ai-memes/grpc_client/grpc_client.py
	import tensorflow as tf
	
	def use_CPU_for_Tensorflow(self): # hay q poner self de parametro porque siempre manda self de parametro
        # para hacer que tensorflow use cpu
        
        print(tf.__version__)

        # Set CPU as available physical device
        my_devices = tf.config.experimental.list_physical_devices(device_type='CPU')
        tf.config.experimental.set_visible_devices(devices= my_devices, device_type='CPU')

        # To find out which devices your operations and tensors are assigned to
        #tf.debugging.set_log_device_placement(True)

        # Create some tensors and perform an operation
        a = tf.constant([[1.0, 2.0, 3.0], [4.0, 5.0, 6.0]])
        b = tf.constant([[1.0, 2.0], [3.0, 4.0], [5.0, 6.0]])
        c = tf.matmul(a, b)

        print(c)
        # para hacer que tensorflow use cpu

if __name__ == '__main__':
    Client().use_CPU_for_Tensorflow() # para que tensorflow use cpu
	# etc

4) start docker


5)
docker-compose up