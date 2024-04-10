# Router.py

class Router:
    def __init__(self, brand, model, ip_address):
        self.brand = brand
        self.model = model
        self.ip_address = ip_address
        self.connected_devices = []

    def connect_device(self, device):
        self.connected_devices.append(device)
        print(f"{device} connected to the router.")

    def disconnect_device(self, device):
        if device in self.connected_devices:
            self.connected_devices.remove(device)
            print(f"{device} disconnected from the router.")
        else:
            print(f"{device} is not connected to the router.")

    def show_connected_devices(self):
        print("Connected devices:")
        for device in self.connected_devices:
            print(device)

# Example usage:
router = Router("Cisco", "RV160", "192.168.1.1")
router.connect_device("Desktop PC")
router.connect_device("Smartphone")
router.show_connected_devices()
router.disconnect_device("Desktop PC")
router.show_connected_devices()
