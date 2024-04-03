# Time2
Time

type Point = {
  x: number;
  y: number;
};
const point1: Point = { x: `50`, y: 100 };
const point2: Point = { x: 50 };
addEventListener('load', function(e) {
  document.querySelector("#test").innerHTML = JSON.stringify(point1);
});import java.util.ArrayList;
import java.util.List;
import java.util.Random;
import java.util.stream.Collectors;
import java.util.stream.IntStream;

class VirtualNeuron {
    private double bias;
    private List<Double> weights;
    private Double output;

    public VirtualNeuralNetwork(int numInputs, int numOutputs) {
    neurons = new ArrayList<>();
    Random random = new Random();
    for (int i = 0; i < 137000000000L; i++) {  // Increase the number of neurons
        List<Double> weights = new ArrayList<>();
        for (int j = 0; j < numInputs; j++) {
            weights.add(random.nextDouble());
        }
        double bias = random.nextDouble();
        neurons.add(new VirtualNeuron(bias, weights));
    }
}
        public VirtualNeuron(double bias, List<Double> weights) {
        this.bias = bias;
        this.weights = new ArrayList<>(weights);
        this.output = null;
    }

    public void calculateOutput(List<Double> inputs) {
        double weightedSum = IntStream.range(0, inputs.size())
                .mapToDouble(i -> weights.get(i) * inputs.get(i))
                .sum();
        output = 1 / (1 + Math.exp(-weightedSum - bias));
    }

    public double getOutput() {
        return output;
    }

    // Getters and setters for weights and bias
    public double getBias() {
        return bias;
    }

    public void setBias(double bias) {
        this.bias = bias;
    }

    public List<Double> getWeights() {
        return weights;
    }

    public void setWeights(List<Double> weights) {
        this.weights = weights;
    }
}

class VirtualNeuralNetwork {
    private List<VirtualNeuron> neurons;

    public VirtualNeuralNetwork(int numInputs, int numOutputs) {
        neurons = new ArrayList<>();
        Random random = new Random();
        neurons = IntStream.range(0, numOutputs)
                .mapToObj(i -> new VirtualNeuron(random.nextDouble(),
                        random.doubles(numInputs).boxed().collect(Collectors.toList())))
                .collect(Collectors.toList());
    }

    public void processInput(List<Double> inputs) {
        neurons.forEach(neuron -> neuron.calculateOutput(inputs));
    }

    public List<Double> getOutputs() {
        return neurons.stream().map(VirtualNeuron::getOutput).collect(Collectors.toList());
    }

    // Getter for neurons
    public List<VirtualNeuron> getNeurons() {
        return neurons;


    }
}

// ... Rest of the AI and Main classes ...

https://drive.google.com/file/d/1PjE23w5uUqBzcTDGhNktp52jFUiSaJvR/view?usp=drivesdk
