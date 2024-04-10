import numpy as np
class Network(object):
definit_(self, sizes):
self.num_layers = len(sizes)
self.sizes= sizes
self.biases = [np. random. randn(y, 1) for y in sizes [1:]]
self.weights = [np. random. randn(y, x)
for x, y in zip(sizes [:-1], sizes [1:])]
def feedforward(self, a):
for b, w in zip (self.biases, self.weights):
a = sigmoid(np. dot (w, a) b)
return a
def SGD (self, training_data, epochs, mini_batch_size, eta,
test_data=None):
if test_data: n_test= len(test_data)
n = len(training_data)
for j in xrange (epochs):
random.shuffle(training_data)
mini_batches = [
training_data[k: k mini_batch_size]
for k in xrange(0, n, mini_batch_size)]
for mini_batch in mini_batches: